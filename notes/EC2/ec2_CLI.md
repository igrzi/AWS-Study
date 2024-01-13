# AWS CLI

The AWS Command Line Interface (AWS CLI) is a powerful tool that allows you to interact with various Amazon Web Services (AWS) directly from your command line or terminal. It provides a unified interface for managing AWS services and resources, making it easier to automate tasks and streamline your workflow.

## Create
> aws ec2 describe-instances

This will list all instances configured on your account, it is the same information on can check on your Amazon Console
.
> aws ec2 run-instances --image-id "..." --count 1 --instance-type "..." --key-name "..." --security-group-ids "..." --subnet-id "..."

This command is pretty lengthy, let's dissect it:
- ***aws ec2 run-instances***: This part initiates the process of launching a new EC2 instance.

- ***--image-id***: Specifies the [Amazon Machine Image (AMI)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html) ID.

- ***--count***: Indicates the amount of instances you want to launch.

- ***--instance-type***: Specifies the type of EC2 instance you want to launch, [see here](/notes/EC2/ec2_ec2_instances.md) fore more details.

- ***--key-name***: Specifies the name of the key pair used for securing the instances. This is used for SSH access.

- ***--security-group-ids***: Specifies the security group IDs associated with your instance, this controls inbound and outbound traffic to the instance.

- ***--subnet-id***: Specifies the subnet ID, *subnets* are subdivision of a [Virtual Private Cloud](https://aws.amazon.com/vpc/).

## Delete

> aws ec2 terminate-instances --instance-ids "..."

To terminate an instance you just have to pass it's instance ID as a field parameter and be logged as an authorized user.
