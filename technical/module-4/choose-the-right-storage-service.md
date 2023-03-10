# Choose the Right Storage Service

### Amazon EC2 instance store
Instance store is ephemeral block storage. This is preconfigured storage that exists on the same physical server that hosts the EC2 instance and cannot be detached from Amazon EC2. You can think of it as a built-in drive for your EC2 instance. 

Instance store is generally well-suited for *temporary storage* of information that is constantly changing, such as buffers, caches, and scratch data. It is not meant for data that is persistent or long-lasting. If you need persistent long-term block storage that can be detached from Amazon EC2 and provide you more management flexibility, such as increasing volume size or creating snapshots, then you should use Amazon EBS.

### Amazon EBS
Amazon EBS is meant for data that changes frequently and needs to persist through instance stops, terminations, or hardware failures. Amazon EBS has two types of volumes – *SSD-backed volumes* and *HDD-backed volumes*.

**SSD-backed volumes** have the following characteristics:
* Performance depends on IOPS (input/output operations per second).
* Ideal for transactional workloads, such as databases and boot volumes.

**HDD-backed volumes** have the following characteristics:
* Performance depends on MB/s.
* Ideal for throughput-intensive workloads, such as big data, data warehouses, log processing, and sequential data I/O.

Here are a few important features of Amazon EBS that you need to know when comparing it to other services.
* It is *block storage*.
* You pay for what you provision (you have to provision storage in advance).
* EBS volumes are replicated across multiple servers in a single Availability Zone.
* Most EBS volumes can only be attached to a single EC2 instance at a time.

### Amazon S3
If your data doesn’t change that often, Amazon S3 might be a cost-effective and scalable storage solution for you. Amazon S3 is ideal for storing static web content and media, backups and archiving, and data for analytics. It can also host entire static websites with custom domain names.

Here are a few important features of Amazon S3 to know about when comparing it to other services:
* It is *object storage*.
* You pay for what you use (you don’t have to provision storage in advance).
* Amazon S3 replicates your objects across multiple Availability Zones in a Region.
* Amazon S3 is not storage attached to compute.

### Amazon Elastic File System (Amazon EFS) and Amazon FSx
You learned that S3 uses a flat namespace and isn’t meant to serve as a standalone file system. You also learned most EBS volumes can only be attached to one EC2 instance at a time. So, if you need file storage on AWS, which service should you use?

For file storage that can mount on to multiple EC2 instances, you can use *Amazon Elastic File System (Amazon EFS)* or *Amazon FSx*. The following table provides more information about each service.

<table>
	<thead>
		<tr>
			<th><span>Service</span></th>
      <th><span>Description</span></th>
      <th><span>FAQs</span></th>
		</tr>
	<thead>
		<tbody>
      <tr>
        <td><span><strong>Amazon Elastic File System (Amazon EFS)</strong></span></td>
        <td><span>Fully managed NFS file system</span></td>
        <td><a href="https://aws.amazon.com/efs/faq/" rel="noopener noreferrer" target="_blank" tabindex="0" aria-hidden="false"><span>EFS FAQs</span></a></td>
      </tr>			
      <tr>
        <td><span><strong>Amazon FSx for Windows File Server</strong></span></td>
        <td><span>Fully managed file server built on Windows Server that supports the SMB protocol</span></td>
        <td><a href="https://aws.amazon.com/fsx/windows/faqs/?nc=sn&amp;loc=8" rel="noopener noreferrer" target="_blank" tabindex="0" aria-hidden="false"><span>FSx for Windows File Server FAQs</span></a></td>
      </tr>
      <tr>
        <td><strong>Amazon FSx for Lustre</strong></td>
        <td>Fully managed Lustre file system that integrates with S3</td>
        <td><a href="https://aws.amazon.com/fsx/lustre/faqs/?nc=sn&amp;loc=5" rel="noopener noreferrer" target="_blank" tabindex="0" aria-hidden="false">FSx for Lustre FAQs</a></td>
      </tr>
		</tbody>
</table>

Here are a few important features of Amazon EFS and Amazon FSx to know about when comparing them to other services:
* It is *file storage*.
* You pay for what you use (you don’t have to provision storage in advance).
* Amazon EFS and Amazon FSx can be mounted onto multiple EC2 instances.

## Resources
* [AWS: Storage](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Storage.html)
* [AWS: Cloud Storage on AWS](https://aws.amazon.com/products/storage/)
* [Amazon EFS: How It Works](https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html)
* [Amazon FSx for Windows File Server](https://aws.amazon.com/fsx/windows/)
* [Amazon FSx for Lustre:](https://aws.amazon.com/fsx/lustre/)