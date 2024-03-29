# Database-as-a-Service

## Multi-AZ
* SYNCHRONOUS replication from the primary instance to the stand-by replica instance
* Provides HA but not fault tolerance.
* Failvoer typically happens 60-120 after failure is detected
* When failure heppens the CNAME will then failover to the stand-by replica instance
* Standy-by cannot be used or accessed directly unless a failure happens
* Same region only
* Backup are taken from the stand-by instance which removes performance impact from the primary instance
* Not available to Free-tier

## Backups
* Backups are stored in an AWS managed S3 buckets
* Automated Backups or Manual Snapshots

## Read Replica
* ASYNCHRONOUS replication
* Can be in a different Availability Zone or AWS Region
* Can be promoted as a new read-write database instance when the primary is unavailable resulting to low RTO
* Malwares, data corruction, etc. are replicated; Backups or snapshots must be used to recover in this scenario
* Imporves global availability by using cross-region Read Replica
* Read-only until promoted
