# [AWS Technical Essentials](https://explore.skillbuilder.aws/learn/course/external/view/elearning/1851/aws-technical-essentials?dt=tile&tile=fdt)

### Introduction to Amazon Web Services
* [Overview of Amazon Web Services](https://docs.aws.amazon.com/pdfs/whitepapers/latest/aws-overview/aws-overview.pdf)
* [What is AWS?](module-1/what-is-aws.md)
* [AWS Global Infrastructure](module-1/global-infrastructure.md)
* [Interacting with AWS](module-1/interacting-with-aws.md)
* [Security and the AWS Shared Responsibility Model](module-1/security-and-shared-responsibility.md)
* [Protect the AWS Root User](module-1/protect-aws-root-user.md)
* [Identity and Access Management](module-1/aws-iam.md)
* [Role-Based Access in AWS](module-1/role-based-access.md)

### AWS Compute
* [Compute as a Service](module-2/compute-as-a-service.md)
* [Amazon Elastic Compute Cloud](module-2/amazon-ec2.md)
* [Amazon EC2 Instance Lifecycle](module-2/aws-ec2-instance-lifecycle.md)
* [Container Services](module-2/container-services.md)
* [Serverless](module-2/serverless.md)
* [AWS Lambda](module-2/aws-lambda.md)

### AWS Networking
* [Networking](module-3/networking.md)
* [Amazon Virtual Private Cloud](module-3/amazon-vpc.md)
* [Amazon VPC Routing](module-3/amazon-vpc-routing.md)
* [Amazon VPC Security](module-3/amazon-vpc-security.md)

### AWS Storage
* [Storage Types](module-4/storage-types.md)
* [Amazon EC2 Instance Storage and Amazon Elastic Block Store](module-4/aws-ec2-instance-and-ebs-storage.md)
* [Object Storage with Amazon Simple Storage Serivce](module-4/aws-object-storage-with-s3.md)
* [Choose the Right Storage Service](module-4/choose-the-right-storage-service.md)

### AWS Databases
* [Databases on AWS](module-5/aws-databases.md)
* [Amazon Relational Database Service](module-5/aws-rds.md)
* [Amazon DynamoDB](module-5/aws-dynamodb.md)
* [Choose the Right Database Service](module-5/choose-the-right-db-service.md)

### Monitoring, Optimization, and Serverless
* [Monitoring](module-6/monitoring.md)
* [Amazon CloudWatch](module-6/aws-cloudwatch.md)
* [Solution Optimization](module-6/solution-optimization.md)
* [Traffic Routing with Amazon Elastic Load Balancing](module-6/aws-elb.md)
* [Amazon EC2 Auto Scaling](module-6/aws-ec2-auto-scaling.md)

## Knowledge Check
1. What are the four main factors you should take into consideration when choosing a Region?
   
   a. Latency, high availability, taxes and compliance
   
   **b. Latency, price, service availability, and compliance**
   
   c. Latency, taxes, speed, and compliance
   
   d. Latency, security, high availability, and resiliency

2. Which of the following best describes the relationship among Regions, Availability Zones, and data centers?

   a. Availability Zones are clusters of Regions. Regions are clusters of data centers. 

   b. Data centers are cluster of Availability Zones. Regions are clusters of Availability Zones.

   **c. Regions are clusters of Availability Zones. Availability Zones are clusters of data centers.**

   d. Data centers are clusters of Regions. Regions are clusters of Availability Zones.

3. Which of the following is a benefit of cloud computing?

   a. Run and maintain your own data centers

   b. Increase time to market

   c. Overprovision for scale

   **d. Go global in minutes**

4. Which of the following is a best practice when securing an AWS root user? (Select TWO.)

   **a. Enable multi-factor authentication (MFA) for the root user**

   b. Use the root user for routine administrative tasks

   c. Share the root user credentials with trusted colleagues

   **d. Disable or delete the access keys associated with the root user**

   e. Place root user password in a secure container

5. What does an Amazon EC2 instance type indicate?

   a. Instance placement and instance size

   **b. Instance family and instance size**

   c. Instance tenancy and instance billing

   d. Instance AMI and networking speed

6. Which of the following is true about serverless?

   a. You must provision and manage servers

   b. You must manually scale serverless resources

   c. You must manage availability and fault tolerance

   **d. You never pay for idle resources**

7. Which of the following pieces of information do you need to create a virtual private cloud (VPC)?

   a. Availability Zone it will reside in 

   b. Subnet it will reside in

   c. Group of subnets it will reside in

   **d. AWS Region it will reside in**

8. Which of the following is true for a security group's default setting?

   a. Allows all inbound traffic and blocks all outbound traffic

   **b. Blocks all inbound traffic and allows all outbound traffic**

   c. Allows all inbound and outbound traffic

   d. Blocks all inbound and outbound traffic

9. A network access control list (network ACL) filters traffic at the EC2 instance level.

   a. True 

   **b. False**

10. Which of the following is a typical use case for Amazon Simple Storage Service (Amazon S3)?

   **a. Object storage for media hosting**

   b. Object storage for a boot drive

   c. Block storage for an EC2 instance

   d. File storage for multiple EC2 instances

11. Bucket names must be unique across all AWS accounts.

   **a. True**

   b. False

12. An employee at a healthcare facility is tasked with storing 7 years of patient information that is rarely accessed. Which storage tier should they use? 

   **a. S3 Glacier Deep Archive**

   b. S3 Standard

   c. S3 Standard-Infrequent Access

   d. S3 Intelligent-Tiering

13. An AWS architect is choosing a database for a dataset that has variation within the data. Not every piece of data shares the same attributes. What database should they choose for the solution? 

   a. Amazon Relational Database Service

   b. Amazon Neptune

   **c. Amazon DynamoDB**

   d. Amazon QLDB

14. When using Amazon Relational Database Service (Amazon RDS), what task is the customer responsible for when running and operating the database?

   **a. Optimizing the database**

   b. Provisioning and managing the underlying infrastructure

   c. Installing the RDBMS onto the DB instance

   d. Installing patches to the OS for the DB instance

15. What are the three components of EC2 Auto Scaling?

   **a. Launch template, scaling policies, EC2 Auto Scaling group**

   b. Scaling policies, security group, EC2 Auto Scaling group

   c. Security group, instance type, key pair

   d. AMI ID, instance type, storage

16. Which features are included with Elastic Load Balancing? (Select TWO)

   **a. Integration with Auto Scaling**

   b. AI for categorizing employee photos

   c. Vertical Scaling for EC2 instances

   **d. Directing  incoming traffic to instances**

   e. Deploying new instances as required

17. What are the possible states of a metric alarm? 

   a. OK, ALARM, NOT_AVAILABLE

   **b. OK, ALARM, INSUFFICIENT_DATA**

   c. OK, ALERT, INSUFFICIENT_DATA

   d. OK, ALERT, NOT_AVAILABLE

18. What are the four main factors to consider when choosing a Region?

   **a. Latency, price, service availability, compliance**

   b. Latency, high availability, taxes, compliance

   c. Latency, taxes, speed, compliance

   d. Latency, security, high availability, resiliency

19. Which of the following accurately describes the relationships among Regions, Availability Zones, and data centers?

   **a. Regions are clusters of Availability Zones. Availability Zones are clusters of data centers.**

   b. Availability Zones are clusters of Regions. Regions are clusters of data centers.

   c. Data centers are cluster of Availability Zones. Regions are clusters of Availability Zones.

   d. Data centers are clusters of Regions. Regions are clusters of Availability Zones.

20. Which of the following can be found in an IAM policy? (Select TWO.)

   **a. Effect**

   **b. Action**

   c. Object

   d. Cause

   e. Result

21. Users in a company are authenticated in the corporate network, and they want to use AWS services without signing in again. Which AWS authentication option should the company use?

   **a. IAM role**

   b. AWS root user

   c. IAM user

   d. IAM group

22. Which actions must be completed to allow resources in a public subnet to communicate with the internet?

   **a. Attach an internet gateway to the VPC**

   **b. Create a route in a route table to the internet gateway**

   c. Create a route to a private subnet

   d. Connect resources to a VPN

   e. Disable the firewall

23. What does an Amazon EC2 instance type indicate? 

   **a. Instance family and instance size**

   b. Instance placement and instance size

   c. Instance tenancy and instance billing

   d. Instance AMI and networking speed

24. What is a typical use case for Amazon S3?

   **a. Object storage for media hosting**

   b. Object storage for a boot drive

   c. Block storage for an EC2 instance

   d. File storage for multiple EC2 instances

25. An employee at a healthcare facility is tasked with storing 7 years of patient information that is rarely accessed. Their boss wants them to consider one of the Amazon S3 storage tiers to store the information. Which storage tier should be used?

   a. S3 Standard

   **b. S3 Glacier Deep Archive**

   c. S3 Standard-Infrequent Access

   d. S3 Intelligent-Tiering

26. When using Amazon Relational Database Service, which database task is the customer's responsibility? 

   **a. Optimizing the database**

   b. Provisioning and managing the underlying infrastructure

   c. Installing the RDBMS onto the DB instance

   d. Installing OS patches for the DB instance

27. A Multi-AZ deployment is beneficial when a customer wants to increase the availability of their database. 

   **a. True**

   b. False

28. What are the three components of EC2 Auto Scaling?

   **a. Launch template, scaling policies, EC2 Auto Scaling group**

   b. Scaling policies, security group, EC2 Auto Scaling group

   c. Security group, instance type, Key pair

   d. AMI ID, instance type, storage

29. Which ELB load balancer type should be used for an application that uses a rule based on a website's domain to choose target groups?

   **a. Application Load Balancer**

   b. Classic Load Balancer

   c. Network Load Balancer

   d. Target Load Balancer