---
template: note
last_reviewed: "2022-10-02"
---
![tp.web.random_picture](https://images.unsplash.com/photo-1523474253046-8cd2748b5fd2?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY2MTU3NjExNA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-15) | (time:: 17:30) | (weather:: Vadodara: 🌦   +27°C ↗13km/h)

# AWS IAM Policy

## IAM Policy
- A policy is an object in AWS that, when associated with an identity or resource, defines their permissions.
- IAM comes with managed policies.
- We can create **[inline policy](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_managed-vs-inline.html#inline-policies)** that we can attach directly to a single user, group, or role.
- We can also create custom policies through a Visual editor or JSON editor.

## IAM Policies Structure
- IAM Policy is a JSON document that are made up of [elements](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements.html).
- An IAM Policy document consists of:
	- **Version**: Policy language verion, always use **`2012-10-17`**.
	- **Id**: Policy identifier (optional).
	- **Statement**: One or more individual statemnts (required).
- **Statement** consists:
	- **Sid**: Statement identifier (optional).
	- **Effect**: Whether the statement allows or denies access (`Allow` / `Deny`)
	- **Principal**: account/user/role to which this policy is applied to.
	- **Action**: List of actions this policy allows or denies based on the Effect.
	- **Resource**: List of resources to which the actions applied to.
	- **Condition**: conditions for when this policy is in effect (optional).
> [!MEMORY] Latest Policy Version
> "Version": "2012-10-17"

```JSON
{
	"Version": "2012-10-17",
	"Id": "S3-Account-Permissions",
	"Statement": [
		{
			"Sid": "1",
			"Effect": "Allow",
			"Principal": {
				"AWS": ["arn:aws:iam::12345678912:root"]
			},
			"Action": [
				"s3:GetObject",
				"s3:PutObject"
			],
			"Resource": ["arn:aws:s3:::myBucket/*"]
		}
	]
}
```

## References
- https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html#access_policies-json
- https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html
- https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements.html
---
## Internal Links
[[2022-09-15]], [[AWS]], [[AWS IAM]], [[AWS Certified Solutions Architect - Associate|SAA-C03]]