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

