# Data Lifecycle Manager

![AWS EBS Snapshot Policy](https://d1.awsstatic.com/amazon-data-lifecycle-manager/Diagram1.08dac4488d3d51a6c27c75dc2c751803e8eca43a.png)

You need to create and specify a **tag** and the ***Data Lifecycle Manager*** will create a backup routine for all volumes/instances with this specified tag.  
Then you can define a **routine** for this backup process where you can specify:

- Time frame for running this routine.
- Backup starting time, the snapshot starts being created within one hours of the starting time.
- Retention type. Here you can use two retention options:
    - Count: Here you specify the amount of snapshots/backups you can have at any given time for this volume.
    - Time: With this option you can specify the amount of time the snapshot will be saved, with a interval of ***days, weeks, months or years.***

This is a valuable tool, because it helps you to automate a important feature, but it can also help you to:
- Protect valuable data by enforcing regular backup schedules.
- Retain backups in case of any problems.
- Reduce storage costs by automatically deleting outdated backups.
- Create disaster recovery backup policies that backup data to isolated Regions or accounts.

When combined with the features of [Amazon EventBridge](ec2_eventbridge.md) and [AWS CloudTrail](ec2_cloudtrail.md), it provides a complete and complex backup solution for EC2 instances and individual EBS volumes.

### Important
- It can't manage snapshots or AMIs created by any other means.
- It can't automate creation, retention and deletion of instance store-backed AMIs.