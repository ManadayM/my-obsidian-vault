---
template: note
last_reviewed: "2022-10-02"
---
![tp.web.random_picture](https://images.unsplash.com/photo-1523474253046-8cd2748b5fd2?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY2MTU3NjExNA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-08) | (time:: 18:36) | (weather:: Vadodara: ⛅️  +34°C ↙13km/h)

# AWS IAM
- AWS **Identity and Access Management (IAM)** is a **global service** (i.e. it is not region specific) to control AWS resources and manage users and groups.
- Root account should never be used or shared. Check [[Before starting the AWS learning journey]].
- **"Users" and "Groups" are for people, "Roles" are for machines.**
- An IAM group is a collection of IAM users.
- An IAM Group cannot contain other IAM group(s).
- "Permissions" are governed by "[[AWS IAM Policy|Policies]]" which are in JSON format.
- IAM Group lets you specify permissions for group users. It is easier and ideal to manage permissions on a group level.
- **A group is not an identity and cannot be identified as a principal in an IAM policy**.
- IAM groups cannot be used to group EC2 instances.
- In AWS apply the **least privilege principle**: don't give more permissions than a user needs.

## IAM MFA Options
- **Virtual MFA device** - Google Authenticator, Authy, etc. Supports multiple tokens on a single device.
- **Universal 2nd Factor (U2F) Security Key** - YubiKey by Yubico (3<sup>rd</sup> party). Supports multiple root and IAM users using a single security key.
- **Hardware Key Fob MFA Device** - e.g. Gemalto (3<sup>rd</sup> party).
- **Hardware Key Fob MFA Device for AWS GovCloud (US)** provided by SurePassID (3<sup>rd</sup> party).

## AWS Access Options
There are 3 ways in which we can access AWS account.
1. **AWS Management Console** - protected by Password + MFA.
2. **AWS Command Line Interface (CLI)** - protected by access keys.
3. **AWS Software Development Kit (SDK)** - for code: protected by access keys.

We can generate Access Keys through AWS Management Console.

Access Key ID ~= username
Secret Access Key ~= password

## IAM Security Tools

**IAM Credentials Report (account-level)**
- A report that lists all your account's users and the status of their various credentials.

**IAM Access Advisor (user-level)**
- Access advisor shows the service permissions granted to a user and when those service were last accessed.
- Use this information to revise your policies and reduce permissions.

## IAM Best Practices
- Don't use *root* account except for AWS account setup.
- One physical user = One AWS user
- Assign users to groups and permissions to groups
- Create a strong password policy
- Use and enforce the use of MFA
- Create and use Roles for giving permissions to AWS Services.
- Audit permissions of your account with the IAM Credentials Report.

## References
- https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html

---
## Internal Links
[[2022-09-08]], [[AWS]], [[AWS Certified Solutions Architect - Associate|SAA-C03]]