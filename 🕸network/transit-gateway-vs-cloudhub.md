# Transit Gateway vs CloudHub

### Transit Gateway
* An actual AWS Service
* Connects multiple VPCs (and on-prem sites) together in hub-and-spoke topology
* Used to allow transitive peering (a VPC limitation) between VPCs
* You don't need a VPC to create (and attach) a Transit Gateway. VPCs attach to the Transit Gateway

#### See:
* [Create a Transit Gateway](https://www.youtube.com/watch?v=E5HpOVKNpug)


### CloudHub
* Not an actual AWS Service
* More like a strategy or approach. You can use a Transit Gateway or your own EC2 Instance router to enable transitive peering
* Uses an Amazon VPC virtual private gateway with multiple customer gateways
* Connects VPC and on-prem together
