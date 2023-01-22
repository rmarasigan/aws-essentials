# Networking
A **Network** is a way of communication between devices. AWS Networking allows creating a fast, reliable, and secure network. AWS offers various cloud services that are on-demand, available, and highly scalable. Various AWS services make an AWS network complete, like Amazon VPC, Amazon EC2, Amazon Route 53, Load Balancers, Amazon Gateway, and more.

## Virtual Private Cloud (VPC)
Amazon Virtual Private Cloud (VPC) creates a virtual network where developers can launch resources in an isolated section of the AWS cloud. Developers use this tool to enable secure communication between different parts of the cloud network, such as Amazon EC2 instances in different subnets.

A virtual network is a private network that is always hidden from the outside world, and you can perform certain operations that you don’t want to make public. Any user with their AWS account can host Amazon VPC. You can create, access, and manage Amazon VPC with the help of certain tools and services like the Amazon Web Service Management Console, Amazon CLI (Command Line Interface), Amazon SDK, and Query API.

### Subnet
A **subnet** is a part of the logical cloud where the instances are to be initiated. It makes a collection of the same to provide safety and sound actions. An Internet entryway has to be given as a supplementary for serving the instances to attain the tune-ups.

**Types of subnet**
* If a subnet’s traffic is routed to an internet gateway, the subnet is known as a **public subnet**.
* If a subnet doesn’t have a route to the internet gateway, the subnet is known as a **private subnet**.
* If a subnet doesn’t have a route to the internet gateway, but has its traffic routed to a virtual private gateway for a VPN connection, the subnet is known as a **VPN-only subnet**.

### Route Table
It is used to direct traffic with a set of rules called routes.

### Internet Gateway
Internet Gateway is the Amazon VPC side of a connection to the public Internet.

### Security Group
It controls the incoming and outgoing crowds and operates as a defense border. You may allow more than one such group while initiating instances. While doing this, you have to specify certain protocols for the incoming crowd as well as for the outgoing crowd. Except for these, all other types of crowds are removed. The protocols for the incoming and outgoing crowds can be adjusted as well.

### Network Access Control List (NACL)
**NACL** helps in providing a firewall thereby helping secure the VPCs and subnets. It helps provide a security layer which controls and efficiently manages the traffic that moves around in the subnets. It is an optional layer for VPC, which adds another security layer to the Amazon service. 

## Security Group vs Network ACL
<table>
  <tbody>
    <tr>
      <th>Security Group</th>
      <th>Network ACL</th>
    </tr>
    <tr>
      <td>Operates at the instance (interface) level</td>
      <td>Operates at the subnet level</td>
    </tr>
    <tr>
      <td>Supports allow rules only</td>
      <td>Supports allow and deny rules</td>
    </tr>
    <tr>
      <td>Stateful</td>
      <td>Stateless</td>
    </tr>
    <tr>
      <td>Evaluates all rules</td>
      <td>Processes rules in order</td>
    </tr>
    <tr>
      <td>Applies to an instance only if associated with a group</td>
      <td>Automatically applies to all instances in the subnets its associated with</td>
    </tr>
  </tbody>
</table>

## AWS Direct Connect
AWS Direct Connect helps in establishing a dedicated network from your premises to AWS. It enables a private and secure connection between AWS and the data center. It is compatible with AWS services and supports a high bandwidth for a more consistent network and better speed. The starting speed is around 50 Mbps and supports scaling up to 100 Gbps. This Amazon networking service uses an Ethernet cable to connect an organization's internal workloads to one of AWS' Direct Connect locations.

This connection creates multiple virtual interfaces to Amazon's publicly accessible cloud services or to private resources hosted on AWS. Users can access private and public resources with the same connection while maintaining network separation between the two environments. AWS Direct Connect is particularly useful for organizations with strict governance and compliance rules that require private connectivity.

## Reference
* [What is AWS Networking? - AWS Networking Services](https://intellipaat.com/blog/tutorial/amazon-web-services-aws-tutorial/networking/)
* [A list of AWS networking services cloud users should know](https://www.techtarget.com/searchcloudcomputing/feature/Boost-cloud-connectivity-with-these-Amazon-networking-services)
* [AWS Network Access Control List - What are its Components?](https://www.knowledgehut.com/tutorials/aws/aws-nacl)
* [AWS Networking Fundamentals – A Brief Introduction for Beginners](https://k21academy.com/amazon-web-services/aws-solutions-architect/networking-fundamental/)