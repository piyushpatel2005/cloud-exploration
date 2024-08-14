# Networking Services

This lesson provides overview of networking services in GCP. There will be detailed lessons for each of these in these set of lessons.

## VPC

In on-prem environment, businesses have greater control on what is connected to the network. It may have a separate physically isolated network from other businesses. In Google Cloud, we can have VPC (Virtual Private Cloud) which can act like a separated cloud from other enterprises. This is software-defined network and can span all across the globe on Google's own private network. VPC is core networking service and is a global resource. These Google Cloud VPCs can also be connected to on-prem network using various mechanisms or there are options to share VPC with other projects in GCP. Each VPC contains a default network and you can easily create new networks. VPCs can be created as Automatic mode which by default creates subnets in all geographic regions across Google cloud and Custom mode in which you specify the CIDR range for each subnet you want to create.

Subnets are simply division of VPC by region. Subnets are regional resources and they have associated IP range for each of the subnets. One important point is that subnets in a single VPC cannot have overlapping IP addresses between two subnets.

### Firewall Rules

Firewall rules are apply to a given project and network. These rules allows you to govern traffic coming into your compute engine instance and also traffic leaving the instance. Every GCP network has two implied rules.

- Implied egress rule which allows all instances to send traffic to any outbound destinations.
- Implied deny rule which denies any IP address and protects all instances by blocking incoming connections to them.

There are also few pre-defined firewall rules which apply to automatically created VPC.  These rules have lowest priority so you can easily define custom rules to override these pre-populated rules. The default network has four firewall rules pre-defined to allow for common access patterns.
1. default-allow-internal: allows incoming connections to VM instances from other instances within a network.
2. default-allow-ssh: This allows you to connect to instances using ssh.
3. default-allow-rdp: This allows to connect to instances using Microsoft Remote Desktop Protocol (RDP).
4. default-allow-icmp: allows you to ping the VM IP addresses.

## Routes

Clodu Router is a fully distributed and managed Google Cloud service that offers advanced networking funtions as a software. It is used to specify how packets leaving a compute instance should be directed to its destination. It uses Border Gateway Protocol (BGP) to advertise IP prefixes and programs dynamic routes based on BGP advertisements it receives from a peer.

## Cloud CDN

This is content delivery service from Google Cloud. If you're using any other CDN service, it's possible that those service providers might be using Google Cloud. CDN enables low-latency response to user requests by caching content on numbers of edge locations across the globe on Google Cloud network. This way when user requests data from anywhere in the world, the request is served with content from nearby location and thus reducing the latency. It's ideal for websites with large amounts of static content like CSS, Javascript and other static contents.

## Load Balancing

A cloud load balancer is used to distribute incoming traffic across multiple instances in the backend applications. You can choose between application load balancer and network load balancer.

### Application Load Balancers

These are application or layer 7 load balancers used to distributed HTTP and HTTPS traffic to backend services hosted on VMs or Kubernetes engine. These load balancers can also distribute traffic based on the content-type of request.

- Application load balancer can be external load balancer which can be deployed in global, regional or classic mode. 
- Internal load balancers can provide internal proxy-based load balancing of application data. This can be deployed in regional or cross-regional modes.

### Network Load Balancing

Network load balancers are layer 4 load balancers that can handle TCP, UDP or other protocol traffic. They are used to distribute traffic among servers in  the same region based on their incoming IP protocol such as address, port or even protocol.

## Google Cloud DNS

Cloud DNS is domain name service in GCP. It's highly available, low-latency service for mapping domain names to IP addresses. Cloud DNS can automatically scale and removes burden of scaling the underlying infrastructure for addresses. You can work with DNS records using CLI, API or Google Cloud SDKs.

## Connectivity Options

There may be situation when you want to connect GCP to your on-premises environment or even to another cloud provider in multicloud set up. Google Cloud providers various options for connecting with different VPC.

### Cloud VPN

Cloud VPN allows you to connect existing network to your VPC through IPSec connection. In this, data travels through the public internet however it is encrypted between these two networks between source and destination gateway. Cloud VPN also comes as a High Availability VPN solution which allows you to connect networks with higher availability.

### Cloud Interconnect

Dedicated Interconnect provides direct physical connections between your on-premises network and Google's network. This connection solution provides high availability, low latency, enterprise-grade connection and is great solution for large amounts of data transfer between two networks. 

To set up **direct interconnect**, your network and Google's network must be in the same colocation facility. There is additional cost for managing this connection, but it provides lowest latency.

If customer's network and Google's network are not in the same colocation facility, the business can choose to use **Partner Interconnect**. This provides connectivity between on-premises network and Google Cloud VPC through a supported service provider. 

### Direct Peering

Network peering allows customers to connect their networks to a Google network's point of access. It uses BGP (Border Gateway Protocol) to exchange routes. It's not a GCP service and can be useful solution when you need to access Google Workspace services on top of Google Cloud services.