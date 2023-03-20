# Solution Optimization

## Availability
The availability of a system is typically expressed as a percentage of uptime in a given year or as a number of nines. In the table, you can see a list of the percentages of availability based on the downtime per year, as well as its notation in nines. 

<table>
  <thead>
    <tr>
      <th>Availability (%)</th>
      <th>Downtime (per year)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>90% (one nine)</td>
      <td>36.53 days</td>
    </tr>
    <tr>
      <td>99% (two nines)</td>
      <td>3.65 days</td>
    </tr>
    <tr>
      <td>99.9% (three nines)</td>
      <td>8.77 hours</td>
    </tr>
    <tr>
      <td>99.95% (three and a half nines)</td>
      <td>4.38 hours</td>
    </tr>
    <tr>
      <td>99.99% (four nines)</td>
      <td>52.60 minutes</td>
    </tr>
    <tr>
      <td>99.995% (four and a half nines)</td>
      <td>26.30 minutes</td>
    </tr>
    <tr>
      <td>99.999% (five nines)</td>
      <td>5.26 minutes</td>
    </tr>
  </tbody>
</table>

To increase availability, you need redundancy. This typically means more infrastructure – more data centers, more servers, more databases, and more replication of data. You can imagine that adding more of this infrastructure means a higher cost. Customers want the application to always be available, but you need to draw a line where adding redundancy is no longer viable in terms of revenue.

### Improve application availability
In the current application, one EC2 instance hosts the application, the photos are served from Amazon Simple Storage Service (Amazon S3), and the structured data is stored in Amazon DynamoDB. That single EC2 instance is a single point of failure for the application.

Even if the database and Amazon S3 are highly available, customers have no way to connect if the single instance becomes unavailable. One way to solve this single point of failure issue is to add one more server.

### Second Availability Zone
The physical location of a server is important. On top of potential software issues at the operating system or application level, hardware issues must be considered. It could be in the physical server, the rack, the data center, or even the Availability Zone hosting the virtual machine. To fix the physical location issue, you can deploy a second EC2 instance in a different Availability Zone. And, the new instance might also solve issues with the operating system and the application. However, having more than one instance brings new challenges.

## Replication, redirection, and high availability
### Replication process
The first challenge with multiple EC2 instances is that you need to create a process to replicate the configuration files, software patches, and application across instances. The best method is to automate where you can.

### Customer redirection
The second challenge is how to let the clients (the computers sending requests to your server) know about the different servers. Various tools can be used here. The most common is using a Domain Name System (DNS) where the client uses one record that points to the IP address of all available servers. However, the time it takes to update the list of IP addresses and for the clients to become aware of such change, sometimes called propagation, is typically the reason why this method isn’t always used.

Another option is to use a load balancer, which takes care of health checks and distributing the load across each server. Situated between the client and the server, a load balancer avoids propagation time issues.

### Types of high availability
The last challenge to address when having more than one server is the type of availability you need – active-passive or active-active.
* **Active-Passive**: With an active-passive system, only one of the two instances is available at a time. One advantage of this method is that for stateful applications where data about the client’s session is stored on the server, there won’t be any issues because the customers are always sent to the server where their session is stored.
* **Active-Active**: A disadvantage of active-passive and where an active-active system shines is scalability. By having both servers available, the second server can take some load for the application, allowing the entire system to take more load. However, if the application is stateful, there would be an issue if the customer’s session isn’t available on both servers. Stateless applications work better for active-active systems.

## Resources
* [High Availability and Scalability on AWS](https://docs.aws.amazon.com/whitepapers/latest/real-time-communication-on-aws/high-availability-and-scalability-on-aws.html)
* [AWS Reliability Pillar: AWS Well-Architected Framework](https://d1.awsstatic.com/whitepapers/architecture/AWS-Reliability-Pillar.pdf)