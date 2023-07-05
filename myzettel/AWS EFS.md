---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1519176901601-d6349438a2b7?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjY0Njk4MTc2&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-10-02) | (time:: 13:39) | (weather:: Vadodara: ⛅️  +33°C →10km/h)

# AWS EFS
- EFS stands for Elastic File System.
- EFS is a **managed network file system** (NFS) that allows you to **mount the same file system on EC2 instances** that are **in different AZs**.
- Highly available, scalable, **3 x gp2** expensive, pay per use.
- Use cases: CMS, Web Serving, data sharing, WordPress.
- Uses NFS v4.1 protocol.
- Uses security group to control access to EFS.
- **Only compatible with Linux-based AMI**.
- The file system scales automatically, no capacity planning is required.

## Scale
- 10 GB+ / second throughput
- Grow to a Petabyte-scale network file system automatically

## Performance mode
- Set at EFS creation time
- **General purpose (default):** latency-sensitive use cases (Web Server, CMS, etc.)
- **Max I/O:** higher latency, throughput, highly parallel (big data, media processing)

## Throughput mode
- **Bursting (Default):** (1 TB = 50 MiB/s + burst of up to 100 MiB/s)
- **Provisioned:** Set your throughput regardless of storage size.

## EFS - Storage Classes
- Storage Tiers
	- **Standard:** Frequently accessed files
	- **Infrequent Access (EFS-IA):** cost to retrieve files, lower price to store.
- Availability and durability
	- **Standard:** Multi-AZ, great for production.
	- **One Zone:** One AZ, great for dev, backup enabled by default, compatible with IA (EFS One Zone IA)
	- Over 90% in cost savings with EFS One Zone IA

---
## Internal Links
[[2022-10-02]], [[AWS]], [[AWS EBS]], [[AWS Certified Solutions Architect - Associate|SAA-C03]]