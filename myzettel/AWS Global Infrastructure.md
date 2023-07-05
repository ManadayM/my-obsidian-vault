---
template: note
last_reviewed: "2022-10-02"
---
![tp.web.random_picture](https://images.unsplash.com/photo-1523474253046-8cd2748b5fd2?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY2MTU3NjExNA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-08) | (time:: 11:50) | (weather:: Vadodara: ⛅️  +32°C ↙9km/h)

# AWS Global Infrastructure
![[AWS Global Infrastructure.png]]
AWS Regions Map as on May 2022. Courtesy: [AWS Getting Started Guide](https://aws.amazon.com/getting-started/cloud-essentials/)

## AWS Regions & Availability Zones
- A Region is a **physical location** in the world **having multiple Availability Zones**.
- **Each region has at least 2 availability zones (AZ)** e.g. `us-east-1a`, `us-east-1b`, `ap-southeast-2a` etc.
- Availability Zones **consist of one or more discrete data centers**, each with redundant power, networking, and connectivity, housed in separate facilities.
- **The smallest number of data centers per region is 2** as Each region has a minimum of 2 AZs and each AZ has a minimum of 1 data center.
- Each AZ is geographically separated for disaster recovery but they are still connected with ultra-low latency networks.
- AZs are connected with a high-speed private link.
- Each AZ runs on its own physically distinct, independent infrastructure and is engineered to be highly reliable.
- **Most AWS services are region-scoped i.e. you provision and pay for services by region.**
- Very few services are inherently multi-region e.g. Aurora Global, and DynamoDB Global.

## Global Infra Statistics
As on September 2022.
- AWS Launched Regions:: 27
- AWS Upcoming Regions:: 7
- AWS Availability Zones:: 87
- AWS Local Zones:: 17
- AWS Wavelength Zones:: 28
- AWS Points of Presence:: 413
- AWS Edge Locations:: 400
- AWS Regional Edge Caches:: 13

## Region Naming Convention
![[AWS Region Naming Convention.png]]

## References
- https://aws.amazon.com/about-aws/global-infrastructure/
- https://aws.amazon.com/about-aws/global-infrastructure/regions_az/
- https://tutorialsdojo.com/aws-global-infrastructure/
---
## Internal Links
[[2022-09-08]], [[AWS]], [[AWS Certified Solutions Architect - Associate|SAA-C03]] 