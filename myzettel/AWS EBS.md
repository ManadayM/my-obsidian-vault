---
template: note
last_reviewed: "2022-10-02"
---
![tp.web.random_picture](https://images.unsplash.com/photo-1523474253046-8cd2748b5fd2?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY2MTU3NjExNA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-21) | (time:: 17:35) | (weather:: Vadodara: ⛅️  +32°C →18km/h)

# AWS EBS
- EBS stands for **Elastic Block Store**.
- **An EBS Volume is a network drive** you can attach to your instances while they run.
- It uses the network to communicate with the instance, meaning there might be a bit of latency.
- Allows persisting data, even after their termination.
- Can be detached from an EC2 instance and attached to another one quickly.
- **Locked to a specific availability zone.**
- Create a snapshot to move it to another AZ.
- Have a provisioned capacity (Size in GBs and IOPS)

> [!MEMORY] Analogy
> Think of them as a "network USB stick".

> [!NOTE] Free Tier
> 30 GB of free EBS storage of type General Purpose (SSD) or Magnetic per month.

## EBS Snapshots & Features
- **EBS Snapshot is a backup of your EBS volume at a point in time.**
- Not necessary to detach the volume to take the snapshot, but recommended.
- Can copy snapshots across AZ or Regions.
- **EBS Snapshot Archive**
	- "Archive Tier" is 75% cheaper
	- Takes 24 to 72 hours for restoring the archive
- **Recycle Bin for EBS Snapshots**
	- Setup rules to retain deleted snapshots so you can recover them after an accidental deletion
	- Retention - 1 day to 1 year
- **Fast Snapshot Restore (FSR)**
	- Force full initialization of snapshot to have no latency on the first use (\$\$\$)

## EC2 Instance Store
- EBS volumes are network drives with good but **limited** performance.
- For a **high-performance hardware disk**, use EC2 Instance Store.
- **EC2 Instance Store lose their storage if they're stopped**
- **Use cases:** buffer, cache, scratch data, and temporary content.
- Backups and replication are your responsibility.

## EBS Volume Types
> [!MEMORY] Imp for Exam
> gp2 and provisioned IOPS are going to be the most important concepts for the exam.
- EBS Volume Types come in 6 types
	- **gp2 / gp3 (SSD):** 
		- General purpose SSD volume that balances price and performance for a wide variety of workloads.
		- Size can vary from **1 GiB to 16 TiB**
	- **io 1 / io 2 (SSD):** Highest-performance SSD volume for mission-critical low latency or high-throughput workloads.
	- **st 1 (HDD):** Low-cost HDD volume designed for frequently accessed, throughput-intensive workloads.
	- **sc 1 (HDD)**: Lowest-cost HDD volume designed for less frequently accessed workloads.
- **Only gp2/gp3 and io1/io2 can be used as boot volumes.**

### General Purpose SSD
#### GP2
- Can burst to 3,000 IOPS,
- The size of the volume and IOPS are linked, the max IOPS is 16,000.
- 3 IOPS per GB, which means at 5,334 GB we are at the max IOPS.

#### GP3
- The newer generation with baseline IOPS of 3,000 and a throughput of 125 MiB/s.
- Can increase IOPS up to 16,000 and throughput up to 1,000 MiB/s **independently**.

### Provisioned IOPS SSD (PIOPS)
- Critical business applications with sustained IOPS performance.
- Or applications that need more than 16,000 IOPS.
- Great for database workloads (Sensitive to storage perf and consistency)
- **Io 1 or io 2** - 4 GiB - 16 TiB
	- Max IOPS 64,000 for Nitro EC2 instances & 32,000 for other.
	- Can increase PIOPS independently from storage size
	- **io2 SSDs have more durability and more IOPS per GiB - at the same price as io1**
	- **io2 Block Express** - 4 GiB - 64 TiB
		- Sub-millisecond latency
		- Max PIOPS 256,000 with an IOPS:GiB ratio 1,000:1
	- Supports EBS Multi-attach.

### Hard Disk Drives (HDD)
- Cannot be a boot volume
- 125 MiB to 16 TiB
- Throughput Optimized HDD (**st1**)
	- Big data, Data warehouses, Log processing
	- Max throughput 500 MiB/s - max IOPS 500
- Cold HDD (**sc1**)
	- For data that is infrequently accessed
	- Scenarios where the lowest cost is important
	- Max throughput 250 MiB/s - max IOPS 250

## EBS Multi-Attach - io1 & io2 family
- **Attach the same EBS volume to multiple EC2 instances in the same AZ.**
- Each instance has full read & write permissions to the high-performance volume.
- Use case:
	- Higher application availability in clustered Linux apps (ex: Teradata)
	- Apps must manage concurrent write operations
- **Up to 16 EC2 instances at a time.**
- Must use a cluster-aware file system (not XFS, EX4, etc...)

## EBS Encryption
- When you create an encrypted EBS volume, you get the following
	- Data at rest is encrypted inside the volume
	- All the data in flight mode b/w the instance and the volume is encrypted 
	- All snapshots are encrypted
	- All volumes created from the snapshot
- You don't have to do anything for Encryption and Decryption.
- EBS Encryption leverages keys from KMS (AES-256)

---
## Internal Links
[[2022-09-21]], [[AWS]], [[AWS EC2]], [[AWS Certified Solutions Architect - Associate|SAA-C03]], [[File Systems]], [[AWS EFS]] 