# EC2 Pricing Models
## Introduction
### EC2 Pricing Model
* On-Demand (Least Commitment)
  * Low cost and flexible
  * only pay per hour
  * short-term, spiky, unpredictable workloads
  * cannot be interrupted
  * For first time apps
* Spot - upto 90% (Biggest Savings)
  * Request spare computing capacity
  * Flexible start and end times
  * Can handle interruptions (server randomly stopping and starting)
  * For non-critical background jobs
* Reserved - upto 75% off (Biggest long-term)
  * Steady state or predictable usage
  * commit to EC2 over 1 or 3 year term
  * Can resell unused reserved instances
* Dedicated (Most expensive)
  * Dedicated servers
  * Can be on-demand or reserved (upto 70% off)
  * When you need a guarantee of isolate hardware (enterprise requirements)

### On-demand instances (Least Commitment)
* When you launch an EC2 instance it is by default using On-demand Pricing
* On-demand has no **up-front payment** and no **long-term commitment**
* You are charged by the **hour** or by the **minute** (varies based on EC2 Instance Types)
* **On-demand** is for application wher e the workload is for the **short-term, spikey, or unpredictable**: when you have a **new app** for development or you want to run experiment.

### Reserved Instances (Biggest Long-Term Savings)
* Best long-term savings
* Designed for applications that have a steady-state, predictable usage, or require reserved capacity.
* Reduced pricing is based on: **Term x Class offering x Payment Option**
* Class Offerings
  * **Standard:** Up to 75% reduced pricing compared to on-demand. Cannot change RI attributes.
  * **Convertible:** Up to 54% reduced pricing compared to on-demand. Allows you to change RI attributes if greater or equal in value
  * **Scheduled:** you reserve instances for specific time periods (eg. once a week for a few hours. Savings vary)
* Terms: you commit to a 1 Year or 3 Year contract. The longer the term the greater savings.
* Payment Options: All upfront, partial upfront, or no upfront
* The greater the upfront the greater the savings
* RIs can be shared between multiple accounts within an org
* Unused RIs can be sold in the Reserved Instance Marketplace

### Spot Instances (Biggest Savings)
* AWS has **unused compute capacity** that they want to maximize the utility of their idle servers.
* It's like hwen a hotel offers discounts for unfilled vacant suites or planes offer discount to fill vacant seats.
* Spot instances provide a discount of **90%** compared to <u>On-Demand Pricing</u>.
* Spot instances can be terminated if the computing capacity is needed by on-demand customers
* Designed for applications that have flexible start and end times or applicatio that are only feasible at very low compute costs.
* **AWS Batch** is an easy and convenient way to use Spot Pricing
*  Termination Conditions: 
   *  If your instance is terminated by AWS, you don't get charged for a partial hour of usage.
   *  Uf you terminate an instance you will still be charged for any hour that it ran

### Dedicated Host Instances (Most Expensive)
* Designed to meet regulatory requirements. When you have **strict server-bound** licensing that won't support multi-tenancy or cloud deployments
* Multi-Tenant
  * When multiple customers are running workloads on the same hardware, **Virtual Isolation** is what separates customers (think apartment).
* Single Tenant
  * When a single customer has dedicated hardware, physical isolation is what separates customers (think house)
  * Offered in both On-demand and Reserved (70% off on-demand pricing)
  * Enterprises and Large Organiztions may have security concerns or obligations against sharing the same hardware with other AWS customers.