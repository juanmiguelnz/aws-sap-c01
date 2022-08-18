## Database-as-a-Service
*
*

## Standby
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
* Read-only until promoted
