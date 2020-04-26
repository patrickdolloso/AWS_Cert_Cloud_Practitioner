# AWS Global Infrastructure
## Introduction and Map Overview
### Where does all this Cloud Computing Run?
* **69** Availability zones within **22** Geographic Regions around the world. Way more edge locations than AZs!
* AWS serves over a million active customers in more than 190 countries
* Steadily **expanding** global infrastructure to help customers achieve lower latency and higher throughput
* **Regions** physical location in the worlds with multiple availability zones
* **Availability Zones** one or more discrete data centers
* **Edge Location** datacenter owned by a trusted partner of AWS

### Regions
* A <b>geographically distinct</b> location which has multiple datacenters (AZs)
* Every region is <b>physically isolated</b> from and independent of every other region in terms of location, power, water supply
* Each region has at least 2 AZs
* AWS largest region is **US-EAST**
* (New) Services almost alwaays become available first in US-EAST
* Not all services are available in all regions
* US-EAST-1 is the region where you see all your billing information

### Availability Zones (AZs)
* An AZ is a datacenter owned and operated by AWS in which AWS services run
* Each region has at least 2 AZs
* AZs are represented by a Region Code, followed by a letter identifier e.g. US-EAST-1a
* **Multi-AZ** Distributing your intances across multiple AZs allows failover configuration for handling requests when one goes down
* <10ms latency between AZs

### Edge Locations
* Get Data Fast or Upload Data Fast to AWS
* An Edge Location is a datacenter owned by a trusted partner of AWS which has a direct connection to the AWS network
* These locations serve requests for **CloudFront** and **Route** **53**. Requests going to either of these services will be routed to the nearest edge location automatically.
* <b>S3 Transfer Acceleration</b> traffic and <b>API Gateway</b> endpoint traffic also use the AWS Edge Network.
* This allows for <b>low latency</b> no matter where the end user is geographically located

## Govcloud Regions
### GovCloud (US)
* AWS GovCloud Regions allow customers to host sensitive <b>Controlled Unclassified Information</b> and other types of regulated workloads.
* GovCloud Regions are only operated by employees who are US citizens on US soil.
* They are **only** accessible to US entities and root account holders who pass a screening process
* Customers can architect secure cloud solutions that comply with:
  * FedRAMP High baseline
  * DOJ's Criminal Justice Information Systems (CJIS) Security Policy
  * US International Traffic in Arms Regulations (ITAR)
  * Export Administration Regulations (EAR)
  * DoD Cloud Computing Security Requirements Guide

