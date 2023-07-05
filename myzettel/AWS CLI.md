---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1523474253046-8cd2748b5fd2?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8bGFuZHNjYXBlLHdhdGVyLG1vdW50YWlufHx8fHx8MTY2MTU3NjExNA&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-15) | (time:: 17:37) | (weather:: Vadodara: 🌦   +27°C ↗13km/h)

# AWS CLI

## What is AWS CLI?
- A tool that enables to interact with AWS Services using commands in your command-line shell.
- Direct access to the public APIs of AWS Services.
- You can develop scripts to manage your resources.
- It's open source https://github.com/aws/aws-cli.
- **The latest version is AWS CLI v2.**
- Alternatively, you can also use the [AWS CloudShell](https://docs.aws.amazon.com/cloudshell/latest/userguide/welcome.html) that is a browser-based, pre-authenticated shell. It can be launched directly from the AWS Management Console. This service is not available in all AWS regions.

### Check the AWS CLI version
```shell
$ aws --version
aws-cli/2.7.32 Python/3.9.11 Darwin/19.6.0 exe/x86_64 prompt/off
```

### Configuration & Named Profiles
- The default location for the AWS CLI configuration is the `.aws` directory inside your operating system's Home directory. For Windows OS it is `%UserProfile%` and for Unix-based systems, it is `$HOME` or `~` (tilde).
- By default, the AWS CLI uses the `default` profile. 
- We can create and use additional named profiles by specifying the `--profile` option and assigning a name. Check the following example where it creates a new profile named `admin`.

```shell
$ aws configure --profile admin
AWS Access Key ID [None]: AKIAI44QH8DHBEXAMPLE
AWS Secret Access Key [None]: je7MtGbClwBF/2Zp9Utk/h3yCo8nvbEXAMPLEKEY
Default region name [None]: us-east-1
Default output format [None]: text
```

Check this [Named profiles for AWS CLI guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html) for more details.

### Using named profile
- Use `--profile <profile-name>` option to use a named profile.
- Set `AWS_PROFILE` environment variable if you intend to execute multiple commands with the same named profile.

```shell
$ export AWS_PROFILE=admin
```

### Change output format
- Use `--output <output-format>` option to override the default format option set.
- Supported format options are `json`, `yaml`, `yaml-stream`, `text`, and `table`.
- Set `AWS_DEFAULT_OUTPUT` environment variable if you intend to execute multiple commands with the same output format.

```shell
$ export AWS_DEFAULT_OUTPUT=json
```

## References
- Getting Started Guide - https://aws.amazon.com/cli/
- AWS CLI Installation Guide - https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
- AWS CLI Setup Guide - https://docs.aws.amazon.com/cli/latest/userguide/getting-started-quickstart.html
- AWS CLI Named Profiles - https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html
- List of AWS CLI Envrionment Variables - https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-envvars.html

---
## Internal Links
[[2022-09-15]], [[AWS]], [[AWS Certified Solutions Architect - Associate|SAA-C03]]