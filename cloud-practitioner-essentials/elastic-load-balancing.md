# Elastic Load Balancing

A managed load balancing service service that distributes incoming application traffic across multiple Amazon EC2 instances, containers, and IP addresses.

* High availability, health checks, security features
* Automatically distributes traffic across multiple resources
* Provides a single point of contact for your Auto Scaling group

<img src = "assets/img/scalability-and-load-balancing.png" width = "60%" /><br />

It enables you to achieve greater levels of fault tolerance in your applications, seamlessly providing the required amount of load balancing capacity needed to distribute application traffic. Elastic Load Balancing detects unhealthy instances and automatically reroutes traffic to healthy instances until the unhealthy instances have been restored. Customers can enable Elastic Load Balancing within a single or multiple Availability Zones for more consistent application performance. Elastic Load Balancing can also be used in an Amazon Virtual Private Cloud ("VPC") to distribute traffic between application tiers in a virtual network that you define.

## Application Load Balancer (HTTP & HTTPS)
Application Load Balancer is best suited for load balancing of HTTP and HTTPS traffic and provides advanced request routing targeted at the delivery of modern application architectures, including microservices and containers. Application Load Balancer routes traffic to targets within Amazon VPC based on the content of the request.

## Network Load Balancer (TCP, TLS, & UDP)
Network Load Balancer is best suited for load balancing of Transmission Control Protocol (TCP), User Datagram Protocol (UDP), and Transport Layer Security (TLS) traffic where extreme performance is required. Network Load Balancer routes traffic to targets within Amazon VPC and is capable of handling millions of requests per second while maintaining ultra-low latencies.

## Gateway Load Balancer
Gateway Load Balancer makes it easy to deploy, scale, and run third-party virtual networking appliances. Providing load balancing and auto scaling for fleets of third-party appliances, Gateway Load Balancer is transparent to the source and destination of traffic. This capability makes it well suited for working with third-party appliances for security, network analytics, and other use cases.