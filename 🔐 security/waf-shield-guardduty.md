### WAF
* Protects web applications from common web exploits
* Filter traffic with rules based on request
* Works with CloudFront, Application Load Balancer, or API Gateway
* Filter by:
  * IP address or country
  * Values in the request (HTTP headers and body, URI strings, length)
  * SQL code - sql injection
  * Scripts - corss-site scripting

### Shield
* Managed DDoS proctection service

### GuardDuty
* Uses Machine Learning to establish a baseline for your normal account activity
* Continually monitors across data sources
  * AWS CloudTrail
  * Amazon VPC Flow Logs
  * DNS Logs
