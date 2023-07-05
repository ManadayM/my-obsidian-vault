---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1523474253046-8cd2748b5fd2?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY2MTU3NjExNA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-26) | (time:: 18:06) | (weather:: Vadodara: ⛅️  +31°C ↘10km/h)

# AWS AMI
- AMI = Amazon Machine Image
- Template for an EC2 instance including configuration, operating system, and data.
- Custom AMIs can be created based on your configuration.
- Commercial AMIs are available in the AWS Marketplace.
- AMIs live in S3, inexpensive to store.
- AMIs can be shared across AWS accounts. If Bob is the author and shares with Alice, then Alice cannot copy the AMI unless Bob has given her permission to EBS snapshot or S3.
- However, if Alice creates an instance from Bob's AMI and then creates an AMI based on that instance, then she'll have a copy of that AMI.
- **You can't launch an EC2 instance using an AMI in another AWS Region, but you can copy the AMI to the target AWS Region and then use it to create your EC2 instances.**

---
## Internal Links
[[2022-09-26]], [[AWS]], [[AWS EC2]], [[AWS Certified Solutions Architect - Associate|SAA-C03]]