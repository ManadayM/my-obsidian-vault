---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1523474253046-8cd2748b5fd2?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY2MTU3NjExNA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-19) | (time:: 17:56) | (weather:: Vadodara: 🌦   +30°C →9km/h)

# AWS EC2
- Amazon Elastic Compute Cloud (EC2) is a web service that provides **resizable compute capacity in the cloud**.
- Consists of:
	- Renting virtual machines (EC2)
	- Storing data on virtual drives (EBS)
	- Distributing load across machines (ELB)
	- Scaling the services using an auto-scaling group (ASG)

## EC2 User Data
- It is possible to bootstrap our instances using an EC2 User Data script.
- **bootstrapping** means launching commands when a machine starts
- That script is **only run once** at the first instance start.
- It is used to automate boot tasks such as:
	- Installing updates
	- Installing software
	- Downloading common files from the internet
	- Anything you can think of
- The EC2 User Data script **runs with the root user**.

## **Instance Types**
- Defines the processor, storage, and memory type.
- Cannot be changed without downtime.
- Pricing is based on the instance type.
- Prices change time-to-time and differ from region to region.
- Categories: 
	- General Purpose
	- Compute, Memory, and Storage Optimized
	- Accelerated computing

## Cheatsheet
- **R:** Applications that need lots of RAM (Memory)
- **C:** Apps that need more compute
- **M:** Middle between R and C (General Purpose)
- **I:** Lots of IO
- **G:** Apps that need GPU power
- **P:** Next generation GPU power (AI, ML, HPC)
- **F:** FPGA-based, comes with Hardware Development Kit (HDK)
- **T2/T3:** Burst-able instances (up to a capacity, uses burst credits)
- **T2/T3:** Unlimited bursts (unlimited burst credits)
- **T4:** Next-gen general purpose burst-able instances based on ARM, 40% more performance than T3
- **X:** Ideal for running large in-memory databases

## Security Groups
> [!MEMORY] Cloud Architect Certification
> You're not required to demonstrate how to properly configure Security Groups. It is important to understand.
- Fundamental of network security in AWS
- They control how traffic is allowed into or out of our EC2 instances.
- Security Group only contains **allow** rules.
- Security Group can be attached to multiple EC2 instances.
- Security Group rules can reference by IP or by security group
- Acts as a firewall on an EC2 instance
- They regulate:
	- Access to ports
	- Authorized IP ranges - IPv4 and IPv6
	- Control inbound network
	- Control outbound network
- **Locked down to a region / VPC combination**
- **It's good practice to maintain one separate security group for SSH access**
- By default, **All inbound traffic is blocked**.
- By default, **All outbound traffic is authorized**.

## Classic Ports to know
- 22 = SSH (Secure Shell) - log into a Linux instance
- 21 = FTP - Upload files into a file share
- 22 = SFTP - Upload files using SSH
- 80 = HTTP - Access unsecured websites
- 443 = HTTPS - Access secured websites
- 3389 = RDP (Remote Desktop Protocol) - log into a Windows instance

## How to SSH using Linux or Mac

```shell
ssh -i YourFile.pem ec2-user@X.X.X.X
```

If you receive error of "Unprotected private key file" as follows then change the file permission using the `chmod 0400 PhantDevServer.cer` command.

```shell
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0644 for '/PhantDevServer.cer' are too open.
It is required that your private key files are NOT accessible by others.
This private key will be ignored.
```

## EC2 Instance Purchase Options
- **On-Demand Instances** - Short workload, predictable pricing, pay by second
	- Linux or Windows - billing per second, after the first minute
	- All other OS - billing per hour
	- **Highest cost, no upfront payment**
	- No long term commitment

- **Reserved (1 & 3 years)**
	- Reserved Instances - Long workloads
	- Convertible Reserved Instances - long workloads with flexible instance types
	- **Up to 72% discount** compared to On-Demand instances
	- Reserve specific instance attributes - Instance Type, Region, Tenancy, OS
	- Reservation period - 1 year (+discount), 3 years (+++discount)
	- Payment Options - No Upfront (+), Partial Upfront (++), All Upfront (+++)

> [!MEMORY] Reserved Instance Marketplace
> You can buy and sell your reserved instances in the Reserved Instance Marketplace.

- **Savings Plan (1 & 3 years)** - Commitment to an amount of usage, long workload
- **Spot Instances** - Short workloads, cheap, can lose instances (less reliable)
	- Can get a discount of up to 90% compared to On-Demand.
	- Define **max spot price** and get the instance while **current spot price < max**.
	- If the **current spot price > your max price** you can choose to **stop** or Reserved Instance Marketplace your instance with a **2 minutes of grace period**.
	- **You can only cancel Spot Instance requests that are Open, active, or disabled.**
	- Canceling **Spot Instance Request** won't terminate already running EC2 instances. It's our responsibility to stop them.
	- **Right order to terminate spot instances is to cancel the Spot Instance Request and then terminate all the spot instances**.
	- **Spot Fleets**
		- The Spot Fleet will try to meet the target capacity with price constraints 
			- Define possible **launch pools**: instance types, OS, availability zone
			- Can have **multiple launch pools**, so that fleet can choose
			- Spot Fleet stops launching instances when reaching capacity or max cost.
		- Strategies to allocate Spot Instances:
			- **lowestPrice**: from the pool with the lowest price (cost optimization, short workload)
			- **diversified**: distributed across pools (great for availability, long workloads)
			- **CapacityOptimized**: pool with the optimal capacity for the number of instances.

> [!MEMORY] Spot Fleets
> Set of Spot Instances + (Optional) On-Demand Instances

- **Dedicated Hosts** - book an entire physical server, control instance placement
- **Dedicated Instances** - no other customers will share your hardware
- **Capacity Reservations** - reserve capacity in a specific AZ for any duration

## References
- https://instances.vantage.sh/ - Nice website to compare all EC2 instances together.

---
## Internal Links
[[2022-09-19]], [[AWS]], [[AWS Certified Solutions Architect - Associate|SAA-C03]] 