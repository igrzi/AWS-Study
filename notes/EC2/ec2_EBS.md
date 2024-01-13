# Amazon Elastic Block Store

It's a storage system in blocks, highly performatic and developed to be used with [Amazon Elastic Compute](ec2_ec2.md).

#### The instance needs to be in the same *region* as the EBS volume.

Some interesting points are:
- Multiple EBS volumes can be attached to the same instance.
- You can attach a EBS volume to **any EC2 instance** in the same availability zone.
- It's like a Hard Drive.

## EBS Benefits
- ***Data disponibility***: When we create a EBS volume, it will be replicated without any additional cost, to prevent lost of any data due to hardware failure.

- ***Data persistence***: A EBS volume is separated from the instance, this means that even if you delete the instance, all the data that was stored will continue to be available, however, **this will be charged**.

- ***Data cryptography***: **All EBS** storage are compatible with cryptography, it even has native cryptography with the use of **AWS Key Management Service (KMS)**.

- ***Snapshots***: Amazon EBS allows the creation of snapshots (backups) of any EBS volume and create a copy of the data inside those volumes to Amazon S3, where data is stored in multiple ***Availability Zones***.

- ***Flexibility***: EBS volumes offer support to changes during production.

## SSD Based Volumes
In here we have two types of drives:
- ***SSD-Backed General Purpose | GP2***: These are a equilibrium between price and perfomance, destined to general purpose workloads.
    - Low latency (milisseconds).
    - Minimum size: 1GB | Maximum size: 16TB
    - Minimum of IOPS: 100 IOPS | Maximum of IOPS: 16.000 IOPS
    - 3 IOPS per GiB base

- ***SSD-Backed Provisioned IOPS | io1***: These are optimized for workloads that require frequent Read/Write with small Input/Output sizes, where the focus is in the number of ***Input/Output Operations Per Second (IOPS)***.
    - Low latency & High performance
    - Minimum size: 4GB | Maximum size: 16TB
    - Minimum of IOPS: 100 IOPS | Maximum of IOPS: 64.000 IOPS
    - The maximum ratio of provisioned iops to requested volume size (in GiB) is 50:1.

## HDD Based Volumes

- ***Throughput Optimized | st1***: *Low cost* HDD volume for frequent acess paired with a high transfer taxes.
    - There isn't compatibility with initializable *st1 volumes*.
    - Minimum size: 500GB | Maximum size: 16TB
    - Maximum of IOPS: 500 IOPS

- ***Cold HDD | sc1***: This is the lowest cost HDD format, destined for less frequent acess.
    - There isn't compatibility with initializable *sc1 volumes*.
    - Minimum size: 500GB | Maximum size: 16TB
    - Maximum of IOPS: 250 IOPS

## EBS Creation CLI
This will display some possible command options:
> aws ec2 help | grep volume


This will initialize a new volume:
> aws ec2 create-volume --availability-zone "..."

Some interesting additional parameters are: 
- ***--availability-zone***: This is the ID of the Availability Zone. For example, us-east-2

- ***--encrypted***: Is a boolean value that indicates if the volume should or shouldn't be encrypted.

- ***--iops***: This is the number of I/O Operations Per Second

- ***--size***: This is an integer that represent the size, in GiB, if you specify a snapshot the default is the snapshot size.

- ***--volume-type***: This specifies the volume type, the options are the ones mentioned in the ***HDD and SSD*** volume types section. **The default volume type is gp2**.

## EBS Attaching CLI

> aws ec2 attach-volume --device "..." --instance-id "..." --volume-id "..."

- ***--device***: The device name (for example, */dev/sdh* or *xvd*)

- ***--instance-id***: ID of the instance you want to attach the volume.

- ***--volume-id***: ID of the EBS Volume. EBS volume and instance should be in the same AZ.

#### To list mounted volumes when doing SSH, type:
> lsblk