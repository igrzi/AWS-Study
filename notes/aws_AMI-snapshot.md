# Snapshots

Snapshots are ***incremental backups***, this means that it only saves the changes done after the latest snapshot. See picture below for reference.

Snapshots are stored in Amazon S3 buckets that you can't acess directly.

We can do data backups inside EBS volumes creating ***point-in-time*** snapshots.


![Incremental Snapshots Example](https://docs.aws.amazon.com/images/AWSEC2/latest/UserGuide/images/snapshot_1a.png)
 

## Cryptography in Snapshots

- Snapshots of cryptographed volumes are automatically cryptographed.

- Volumes created based on cryptographed snapshots are automatically cryptographed.

- When you copy a snapshot that hasn't been encrypted, you can encrypt it during the copying process.