## Database-as-a-Service
*
*

## Multi-AZ
* Synchronous
*

## Backups
*
*

## Read Replica
* Asynchronous
* Can be in a different Availability Zone or AWS Region
* Can be promoted as a new read-write database instance when the primary is unavailable resulting to low RTO
* Malwares, data corruction, etc. are replicated; Backups or snapshots must be used to recover in this scenario
* Imporves global availability by using cross-region Read Replica
* Read-only until promoted
