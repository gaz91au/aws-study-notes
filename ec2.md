## EC2 pricing models 
- on demand
- spot
- reserved
- dedicated - not multi-tenanted

## EC2 Instance Types:
- M - general purpose
- C - compute optimized
- P - graphics optimized
F.I.G.H.T.D.R.M.C.P.X

## Elastic Block Storage
- SSD, general purpose - gp2
- SSD - Provisioned OPS - IO1
- HDD, throughput optimized - ST1
- HDD, cold - SC1
- HDD, magnetic - Standard

- Cant mount 1 EBS to multiple instances.
- Can mount 1 EFS to multiple instances.

- Termination protection is on by default.
- EBS backed instanced is terminated by default.
- EBS backed root volumes can be encrypted using aws api or console, or using 3rd party tools.

## Volumes vs Snapshots
- Volumes exist on EBS, is a virtual hard disk.
- Snapshot exist on S3.
- Snapshots are a point in time of Volumes.
- Snapshots are incremental, first snapshots may take longer.
- Snapshots are encrypted automatically.
- Volumes restored from encrypted snapshots are encrypted automatically.
- You can share snapshots only if its unencrypted.

- You should stop instance before taking snapshots.
- Instance store volumes are sometimes called Ephermeral Storage.
- Instance store volumes cannot be stopped, If host fails, you lose your data.
- EBS backed volumes can be stopped and remain durable.
- You can reboot both Instance store and EBS backed volumes safely.

- By default, root volumes will be deleted on termination.
- With EBS volumes, you can specify to keep root volume.

## Taking snapshot of RAID array
- Snapshots exclude data in cache of applications and OS
- Take application consistent snapshot
    - Stop apps writing to disk
    - Flush all caches to the disk
      1. Freeze the file system
      2. Unmount the RAID array
      3. Shutting down the associated EC2 instance

## AMI 
- AMI are regional
- You can copy AMI's to other regions via cli

## Monitoring
- Standard - 5mins
- Detailed - 1mins

## Cloudwatch 
- Used for performance Monitoring
- Create cool dashboards
- Alarms
- Events
- Logs - aggregate, monitor and store logs

## CloudTrail 
- Auditing

## Roles
- More secure than storing access keys and secrets on EC2 instances
- Roles are easy to manage
- Roles can be assigned to EC2 instance after EC@ has been provisioned
- Roles are universal, all regions (All of IAM is global)

## Instance Meta-data
- Used to get information aboht the instance
- /latest/meta-data
- /latest/user-data

## EFS
- Supports NFS v4 protocol
- Only pay for the storage you user
- Can scale to petabytes
- Supports thousands of concurrent NFS connections
- Data is stored across multiple AZ's within a region

## Placement Groups
- Clustered placement groups - in one AZ
- Spread placement group - across multiple AZ










