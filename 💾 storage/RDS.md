## Database-as-a-Service
*
*

## Multi-AZ
* SYNCHRONOUS replication from the primary instance to the stand-by replica instance
* Provides HA but not fault tolerance. Failvoer typically happens 60-120 after failure is detected

## Backups
*
*

## Read Replica
* ASYNCHRONOUS replication
* Can be in a different Availability Zone or AWS Region
* Can be promoted as a new read-write database instance when the primary is unavailable resulting to low RTO
* Malwares, data corruction, etc. are replicated; Backups or snapshots must be used to recover in this scenario
* Imporves global availability by using cross-region Read Replica
* Read-only until promoted
