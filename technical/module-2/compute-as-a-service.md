# Compute as a Service

### Servers
The first building block you need to host an application is a server. **Servers** usually can handle Hypertext Transfer Protocol (HTTP) requests and send responses to clients following the client-server model, although any API-based communication also falls under this model. A client is a person or computer that sends a request. A server handling the requests is a computer, or collection of computers, connected to the internet serving websites to internet users.

Servers power your application by providing CPU, memory, and networking capacity to process users’ requests and transform them into responses. For context, common HTTP servers include:
* Windows options, such as Internet Information Services (IIS)
* Linux options, such as Apache HTTP Web Server, Nginx, and Apache Tomcat

## Choose the right compute option
If you’re responsible for setting up servers on AWS to run your infrastructure, you have many compute options. You need to know which service to use for which use case. At a fundamental level, three types of compute options are available – *virtual machines (VMs)*, *container services*, and *serverless*.

A **virtual machine** emulates a physical server and allows you to install an HTTP server to run your applications. To run virtual machines, you install a hypervisor on a host machine. The ***hypervisor*** provisions the resources to create and run your VMs.

In AWS, virtual machines are called **Amazon Elastic Compute Cloud**, or Amazon EC2. Behind the scenes, AWS operates and manages the host machines and the hypervisor layer. AWS also installs the virtual machine operating system, called the *guest operating system*.

## Resources
* [Compute Services Whitepaper](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html)
* [Compute on AWS](https://aws.amazon.com/products/compute/)
* [AWS Compute Blog](https://aws.amazon.com/blogs/compute/)
