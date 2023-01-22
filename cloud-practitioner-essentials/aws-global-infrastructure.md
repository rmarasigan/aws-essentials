# Global Infrastructure
The AWS Cloud infrastructure is built around AWS Regions and Availability Zones. An **AWS Region** is a physical location in the world where we have multiple Availability Zones. **Availability Zones** consist of one or more discrete data centers, each with redundant power, networking, and connectivity, housed in separate facilities. These Availability Zones offer you the ability to operate production applications and databases that are more highly available, fault tolerant, and scalable than would be possible from a single data center.

## Regions
AWS has the concept of a **Region**, which is a physical location around the world where we cluster data centers. We call each group of logical data centers an Availability Zone. Each AWS Region consists of a minimum of three, isolated, and physically separate AZs within a geographic area. Unlike other cloud providers, who often define a region as a single data center, the multiple AZ design of every AWS Region offers advantages for customers. Each AZ has independent power, cooling, and physical security and is connected via redundant, ultra-low-latency networks. AWS customers focused on high availability can design their applications to run in multiple AZs to achieve even greater fault-tolerance. AWS infrastructure Regions meet the highest levels of security, compliance, and data protection.

### Criteria for Region Selection
#### Cost
Pricing across AWS Region varies, because of different [CapEx](https://www.bmc.com/blogs/capex-vs-opex/), [OpEx](https://www.bmc.com/blogs/capex-vs-opex/), and regulations in different geographic locations.

#### Service availability
Amazon offers a vast portfolio of cloud-based solutions spanning AWS Regions. While the most popular AWS services are available across all AWS Regions, not every region offers all services.

#### Customer base (latency)
The distance between the cloud deployments (AWS Regions and Zones) and end-users is a key factor that determines the latency and network performance of the cloud service.

#### Regulatory compliance and government policies
* **Regulatory compliance**
  * Specific industry and regulatory specifications—such as the EU’s General Data Protection Regulation (GDPR) and state, provincial, or local locality data handling regulations—may require sensitive end-user data to be processed in specific geographic locations.
* **Data mobility**
  * Cloud computing makes it easy for organizations to transfer, store, and process information in data centers at distant locations, which may be considered as a violation of compliance regulations that may lead to costly lawsuits and damages to the brand reputation.
* **Security requirements**
  * Organizations may also be obliged to distribute workloads across multiple geographically disparate cloud data centers to ensure high availability and security standards of sensitive business information and IT-enabled services.

## Availability Zones
AWS has the concept of a Region, which is a physical location around the world where we cluster data centers. We call each group of logical data centers an **Availability Zone**. Each AWS Region consists of a minimum of three, isolated, and physically separate AZs within a geographic area. Unlike other cloud providers, who often define a region as a single data center, the multiple AZ design of every AWS Region offers advantages for customers. Each AZ has independent power, cooling, and physical security and is connected via redundant, ultra-low-latency networks. AWS customers focused on high availability can design their applications to run in multiple AZs to achieve even greater fault-tolerance. AWS infrastructure Regions meet the highest levels of security, compliance, and data protection.

## Local Zones
AWS Local Zones place compute, storage, database, and other select AWS services closer to end-users. With AWS Local Zones, you can easily run highly-demanding applications that require single-digit millisecond latencies to your end-users such as media & entertainment content creation, real-time gaming, reservoir simulations, electronic design automation, and machine learning.

Each AWS Local Zone location is an extension of an AWS Region where you can run your latency sensitive applications using AWS services such as Amazon Elastic Compute Cloud, Amazon Virtual Private Cloud, Amazon Elastic Block Store, Amazon File Storage, and Amazon Elastic Load Balancing in geographic proximity to end-users. AWS Local Zones provide a high-bandwidth, secure connection between local workloads and those running in the AWS Region, allowing you to seamlessly connect to the full range of in-region services through the same APIs and tool sets.

## Edge Locations
**Edge locations** are Content Delivery Network (CDN) endpoints for CloudFront. They are used by AWS services such as *AWS CloudFront* and *AWS Lambda Edge* to cache data and reduce latency for end-user access by using the Edge Locations as a global Content Delivery Network (CDN). As a result, Edge Locations are primarily used by end users who are accessing and using your services.

## Regional Edge Caches
**Regional Edge Caches** sit between your CloudFront Origin servers and the Edge Locations. A Regional Edge Cache has a larger cache-width than each of the individual Edge Locations. A Regional Edge Cache has a larger cache-width than each of the individual Edge Locations, and because data expires from the cache at the Edge Locations, the data is retained at the Regional Edge Caches.

## Reference
* [AWS Global Cloud Infrastructure: Regions, Zones & More](https://www.bmc.com/blogs/aws-regions-availability-zones/)
* [AWS Global Infrastructure: Availability Zones, Regions, Edge Locations, Regional Edge Caches](https://cloudacademy.com/blog/aws-global-infrastructure/)