# Amazon EC2 Instance Storage and Amazon Elastic Block Store

An ***instance store*** provides temporary block-level storage for your instance. This storage is located on disks that are physically attached to the host computer. Instance store is ideal for temporary storage of information that changes frequently, such as buffers, caches, scratch data, and other temporary content, or for data that is replicated across a fleet of instances, such as a load-balanced pool of web servers.

An ***instance store*** consists of one or more instance store volumes exposed as block devices. The size of an instance store as well as the number of devices available varies by instance type.

***Amazon Elastic Block Store (Amazon EBS)*** provides block level storage volumes for use with EC2 instances. EBS volumes behave like raw, unformatted block devices. You can mount these volumes as devices on your instances. EBS volumes that are attached to an instance are exposed as storage volumes that persist independently from the life of the instance. You can create a file system on top of these volumes, or use them in any way you would use a block device (such as a hard drive). You can dynamically change the configuration of a volume attached to an instance.

## Amazon EC2 Instance Store
Amazon EC2 instance store provides temporary block-level storage for an instance. This storage is located on disks that are physically attached to the host computer. This ties the lifecycle of the data to the lifecycle of the EC2 instance. If you delete the instance, the instance store is deleted, as well. Due to this, instance store is considered ephemeral storage. Read more about it in the [AWS documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html).

Instance store is ideal if you host applications that replicate data to other EC2 instances, such as Hadoop clusters. For these cluster-based workloads, having the speed of locally attached volumes and the resiliency of replicated data helps you achieve data distribution at high performance. It’s also ideal for temporary storage of information that changes frequently, such as buffers, caches, scratch data, and other temporary content.

## Amazon Elastic Block Storage (Amazon EBS)
As the name implies, Amazon EBS is a block-level storage device that you can attach to an Amazon EC2 instance. These storage devices are called Amazon EBS volumes. EBS volumes are essentially drives of a user-configured size attached to an EC2 instance, similar to how you might attach an external drive to your laptop. EBS volumes act similarly to external drives in more than one way.

* Most Amazon EBS volumes can only be connected with one computer at a time. Most EBS volumes have a one-to-one relationship with EC2 instances, so they cannot be shared by or attached to multiple instances at one time. (Recently, AWS announced the Amazon EBS multi-attach feature that enables volumes to be attached to multiple EC2 instances at one time. This feature is not available for all instance types, and all instances must be in the same Availability Zone. Read more about this scenario in the EBS documentation.)
* You can detach an EBS volume from one EC2 instance and attach it to another EC2 instance in the same Availability Zone, to access the data on it.
* The external drive is separate from the computer. That means, if an accident occurs and the computer goes down, you still have your data on your external drive. The same is true for EBS volumes.
* You’re limited to the size of the external drive, since it has a fixed limit to how scalable it can be. For example, you might have a 2-TB external drive, which means you can only have 2 TB of content on it. This relates to EBS as well, since a volume also has a max limitation of how much content you can store on it.

### Scale Amazon EBS volumes
You can scale Amazon EBS volumes in two ways.

* Increase the volume size, as long as it doesn’t increase above the maximum size limit. For EBS volumes, the maximum amount of storage you can have is 16 TB. If you provision a 5-TB EBS volume, you can choose to increase the size of your volume until you get to 16 TB.
* Attach multiple volumes to a single Amazon EC2 instance. EC2 has a one-to-many relationship with EBS volumes. You can add these additional volumes during or after EC2 instance creation to provide more storage capacity for your hosts.

### Amazon EBS use cases
Amazon EBS is useful when you must retrieve data quickly and have data persist long-term. Volumes are commonly used in the following scenarios.

* **Operating systems**: Boot/root volumes to store an operating system. The root device for an instance launched from an Amazon Machine Image (AMI) is typically an Amazon EBS volume. These are commonly referred to as EBS-backed AMIs.
* **Databases**: A storage layer for databases running on Amazon EC2 that rely on transactional reads and writes.
* **Enterprise applications**: Amazon EBS provides reliable block storage to run business-critical applications.
* **Throughput-intensive applications**: Applications that perform long, continuous reads and writes.

### Amazon EBS volume types
Amazon EBS volumes are organized into two main categories – solid-state drives (SSDs) and hard-disk drives (HDDs). SSDs provide strong performance for random input/output (I/O), while HDDs provide strong performance for sequential I/O. AWS offers two types of each.

The following chart can help you decide which EBS volume is the right option for your workload.

<table>
  <thead>
    <tr>
      <th>
        Volume Types
      </th>
      <th>
        Description
      </th>
      <th>
        Use Cases
      </th>
      <th>
        Volume Size
      </th>
      <th>
        Max IOPS
      </th>
      <th>
        Max Throughput
      </th>
    </tr>
  </thead>
  <tbody>
	  <tr>
      <td>EBS Provisioned IOPS SSD</td>
      <td>Highest performance SSD designed for latency-sensitive transactional workloads</td>
      <td>I/O-intensive NoSQL and relational databases</td>
      <td>4 GB–16 TB</td>
      <td>64,000</td>
      <td>1,000 MB/s</td>
    </tr>
    <tr>
      <td>EBS General Purpose SSD</td>
      <td>General purpose SSD that balances price and performance for a wide variety of transactional workloads</td>
      <td>Boot volumes, low-latency interactive apps, development, and test</td>
      <td>1 GB–16 TB</td>
      <td>16,000</td>
      <td>250 MB/s</td>
    </tr>
    <tr>
      <td>Throughput Optimized HDD</td>
      <td>Low-cost HDD designed for frequently accessed, throughput-intensive workloads</td>
      <td>Big data, data warehouses, log processing</td>
      <td>500 GB–16 TB</td>
      <td>500</td>
      <td>500 MB/s</td>
    </tr>
    <tr>
      <td>Cold HDD</td>
      <td>Lowest cost HDD designed for less frequently accessed workloads</td>
      <td>Colder data requiring fewer scans per day</td>
      <td>500 GB–16 TB</td>
      <td>250</td>
      <td>250 MB/s</td>
    </tr>
  </tbody>
</table>

### Amazon EBS benefits
Here are the benefits of using Amazon EBS.

* **High availability**: When you create an EBS volume, it is automatically replicated in its Availability Zone to prevent data loss from single points of failure.
* **Data persistence**: The storage persists even when your instance doesn’t.
* **Data encryption**: All EBS volumes support encryption.
* **Flexibility**: EBS volumes support on-the-fly changes. You can modify volume type, volume size, and input/output operations per second (IOPS) capacity without stopping your instance.
* **Backups**: Amazon EBS provides the ability to create backups of any EBS volume.

### Amazon EBS snapshots
Errors happen. One error is not backing up data and then inevitably losing it. To prevent this from happening to you, always back up your data – even in AWS.

Since your EBS volumes consist of the data from your Amazon EC2 instance, you should make backups of these volumes, called snapshots.

EBS snapshots are incremental backups that only save the blocks on the volume that have changed after your most recent snapshot. For example, if you have 10 GB of data on a volume, and only 2 GB of data have been modified since your last snapshot, only the 2 GB that have been changed are written to Amazon Simple Storage Service (Amazon S3).

When you take a snapshot of any of your EBS volumes, the backups are stored redundantly in multiple Availability Zones using Amazon S3. This aspect of storing the backup in Amazon S3 is handled by AWS, so you won’t need to interact with Amazon S3 to work with your EBS snapshots. You manage them in the Amazon EBS console, which is part of the Amazon EC2 console.

EBS snapshots can be used to create multiple new volumes, whether they’re in the same Availability Zone or a different one. When you create a new volume from a snapshot, it’s an exact copy of the original volume at the time the snapshot was taken.

## Resources
* [Amazon Elastic Block Store (Amazon EBS)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html)
* [Amazon EBS FAQs](https://aws.amazon.com/ebs/faqs/)