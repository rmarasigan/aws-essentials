# AWS Global Infrastructure

Infrastructure, like data centers and networking connectivity, still exists as the foundation of every cloud application. In AWS, this physical infrastructure makes up the AWS Global Infrastructure, in the form of Regions and Availability Zones.

## Regions
**Regions** are geographic locations worldwide where AWS hosts its data centers. AWS Regions are named after the location where they reside. For example, in the United States, the Region in Northern Virginia is called the Northern Virginia Region, and the Region in Oregon is called the Oregon Region. AWS has Regions in Asia Pacific, Canada, Europe, the Middle East, and South America.

Each AWS Region is associated with a geographical name and a Region code.

Here are examples of Region codes:
* **us-east-1**: The first Region created in the eastern US area. The geographical name for this Region is N. Virginia.
* **ap-northeast-1**: The first Region created in the northeast Asia Pacific area. The geographical name for this Region is Tokyo.

AWS Regions are independent from one another. Data is not replicated from one Region to another, without explicit customer consent and authorization.

### AWS Region considerations

#### Data Compliance
Enterprise companies often must comply with regulations that require customer data to be stored in a specific geographic territory. If applicable, choose a Region that meets your compliance requirements.

#### Latency
If your application is sensitive to latency (the delay between a request for data and the response), choose a Region that is close to your user base. This helps prevent long wait times for your customers.

#### Pricing
Due to the local economy and the physical nature of operating data centers, prices vary from one Region to another. Internet connectivity, imported equipment costs, customs, real estate, and other factors impact a Region's pricing. Instead of charging a flat rate worldwide, AWS charges based on the financial factors specific to each Region.

#### Service availability
Some services might not be available in some Regions. The AWS documentation provides a table that shows the services available in each Region.

## Availability Zones
Inside every Region is a cluster of **Availability Zones (AZs)**. An AZ consists of one or more data centers with redundant power, networking, and connectivity. These data centers operate in discrete facilities in undisclosed locations. They are connected using redundant high-speed and low-latency links.

AZs also have a code name. Since they are located inside Regions, they can be addressed by appending a letter to the end of the Region code name.

For example:
* **us-east-1a**: An AZ in us-east-1 (N. Virginia Region)
* **sa-east-1b**: An AZ in sa-east-1 (São Paulo Region)
