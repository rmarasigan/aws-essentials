# Amazon Elastic Compute Cloud (Amazon EC2)

![aws ec2](assets/img/aws-ec2.png)

* Use secure, sizable compute capacity
* Boot server instances in minutes
* Pay only for what you use

## How Amazon EC2 Works
![how-ec2-works](assets/img/how-ec2-works.png)

### Instance Types

#### General Purpose
* Balances compute, memory, and networking resources
* Suitable for a broad range of workloads

#### Compute Optimized
* Offers high-performance processors
* Ideal for compute-intensive applications and batch processing workloads

#### Memory Optimized
* Delivers fast performance for memory-intensve workloads
* Well suited for high-performance databases

#### Accelerated Computing
* Uses hardware accelerators to expedite data processing
* Ideal for application streaming and graphics workloads

#### Storage Optimized
* Offers low latency and high input/output operations per seconds (IOPS)
* Suitable for workloads such as distributed file systems and data warehousing applications

### Instance Pricing Options

#### On-Demand
* No upfront costs or minimum contracts
* Ideal for short-term, irregular workloads

#### Spot
* Ideal for workloads with flexible start and end times
* Offers savings over On-Demand prices
* Can withstand interruptions

#### Reserved
* Provides a billing discount over On-Demand pricing
* Requires a 1-year or 3-year term commitment

#### Compute Savings Plan
* Offers up to 72% savings over On-Demand costs for a consistent amount of compute usage
* Requires a 1-year or 3-year term commitment

#### Dedicated Instance
* An EC2 *instance* that runs in a VPC on hardware for a single customer
* Higher cost compared to standard Amazon EC2 instances

#### Dedicated Host
* A *physical server* with EC2 instance capacity for a single customer
* Most expensive Amazon EC2 option