# AMI
### What is an AMI?

***AMI*** means Amazon Machine Image, it's a supported and maintained image provided by AWS that provides the information required to launch an instance with some specific configurations.

[Official AWS Docs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html)

### AMI Life Cycle

![AMI Life Cycle](https://docs.aws.amazon.com/images/AWSEC2/latest/UserGuide/images/ami_lifecycle.png)

## AMI Creation
**You will need an existing instance to make your AMI.**

> aws ec2 create-image --instance-id "..." --name "..."

This will stop your instance, create an AMI, and then reboot it.

#### Some interesting optional parameters:
- ***--description***: This adds a description for your AMI.

- ***--no-reboot***: This will make your instance stop, but not reboot.

We can check more parameters using the following command:

> aws ec2 create-image help

## AMI Sharing
Per default AMIs are **private**, and not global, but you can convert it to **public** at any given time.

When an AMI is shared, ***the owner doesn't change***.  
You can share an AMI with:

- *Other AWS accounts* by using the **account ID**.

- *Other regions* by generating a [snapshot](/notes/aws_AMI-snapshot.md).

### ATTENTION:
- You ***can't copy*** a cryptographed AMI that has been shared with you.

- You ***can't copy*** an AMI with a billing product code that has been shared with you by another account, like Windows AMIs.

## AMI Deletion
You just need an ***image id***.

> aws ec2 deregister-image --image-id "..."  

You can also this as parameters:
> - ***--dry-run***: check if you have the required permission for the action.

We can check more parameters using the following command:

> aws ec2 deregister-image help