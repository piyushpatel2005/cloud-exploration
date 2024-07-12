# Cloud Computing Fundamentals

## What is Cloud?

First question you should be asking is "What is cloud after all?". For some people, it may be only storage that is cloud. Like they store videos and images from their phone and can then access those pictures from any other device anywhere. However, cloud is lot more than that. Cloud is basically a remote location accessible via the internet which provides computing and storage when needed. We can store data in the cloud and it will stored somewhere on the internet and will be accessible anywhere across the world via the Internet. We can also spin up servers whenever we want in any size we want before actually signing a contract to rent server racks.

There are many companies offering Cloud services in various sizes. The major cloud providers are Google, Amazon, Microsoft, Oracle, Alibaba. There are also other small providers like Linode, Digital Ocean which provide smaller set of services but again on the cloud with on-demand access to resources. By the way resources are the computing or storage services you use or provision in the cloud.

From wikipedia definition:
> Cloud computing is the **on-demand** availability of computer system resources, especially data storage (cloud storage) and computing power, **without direct active management** by the user. Large clouds often have functions distributed over **multiple locations**, each of which is a data center. Cloud computing relies on **sharing of resources** to achieve coherence and typically uses **a pay-as-you-go model**, which can help in reducing capital expenses but may also lead to unexpected operating expenses for users.

## Why is Cloud Computing so popular?

Cloud computing provides relatively easier access to computing resources over the internet. Below are some of the advantages.

- **Cost Savings:** Businesses do not need to reserve server racks upfront. This reduces Capex (capital expenditure). Also, this means we do not need to overprovision. Usually, when business needed resources, they would have reserve those servers in data center in advance. This means usually businesses used to reserve extra capacity anticipating future growth, but sometimes those are not even needed. Cloud computing provides pay-as-you-go model which is lot more flexible. If you're using resources today, get them from cloud provider and if you're not using them, remove those. You pay only for what you used.
- **Scalability & Flexibility:** Cloud resources are lot more flexible and cloud providers have spent lots of development efforts to make the systems autoscale. So, if you need lots of resources for any special sale events like black friday, you can request more resources and use them. Once you're done with holidays season, you can deallocate those resources to reduce your cloud bills.
- **Automatic Updates:** Cloud providers are responsible for some of the managed services for OS updates, backups or patching of software systems. This reduces time spent  by SysAdmins on such tasks.
- **Security:** In cloud, security is a shared responsiblity. Cloud providers are responsible for securing the physical locations where the data is stored. They also provide several security features such as encryption at rest with other services providing encryption in transit. However, using these security measures and securing access to sensitive information is responsibility of the business. Cloud providers do provide features and options to control user, group or any other identity access, but business will have to implement them as they see fit.
- **Agility:** Smaller businesses now can scale with as little as few dollars a month to as much as millions of dollars with their business. They are not limited to having large sum of money upfront to start a business. Cloud also provides latest OS updates, machine types, software versions well before on-premise team could implement those. This makes the team lot more agile with latest software updates.
- **Global Network:** Cloud also provides global scale network. If you want to expand to different part of the world, you can simply spin up new set of resources in that region and have your business provide services in that region. Network updates and maintenance is also managed by cloud providers. Also, networking is software defined, so it's easily managed virtually.

## Characteristics of Cloud Computing

- On-demand and self-serve: You can provision resources whenever you need them and this is done through the internet. You do not need to be physically present at any data center to provision a server.
- Access Anywhere: The customers of cloud providers can access those resources over the internet from any where in the world.
- Resource Pooling: The provider has large resource of computing and storage. All users of the cloud provider share resources from this large pool. When a business requests resources, those resources are assigned to a user until they deallocate those resources. This provides economies of scale.
- Resources are Elastic and Flexible: The resources can be scaled up or down based on workload demand for the customer. They are not tied with any contract to use specific amount of resources. Instead, it's very flexible in nature which helps optimize their operating costs.
- Pay-as-You-Go Model: Cloud computing uses pay as you go model. With this model, you're charged only for the services used by the bussiness and not for anything idle. Of course, this needs some configurations on the business side but it can also be automated with autoscaling.

## Cloud History

The first commercial and wide spread cloud provider was Amazon when they launched Amazon Web services (AWS) in 2006. The initial public offering only included very basic services like EC2 or Elastic Compute Cloud. Next, around 2008, Microsoft announced Project Red Dog which was formally released as Windows Azure in 2010. This was later renamed to Microsoft Azure. Google also launched its beta version of Google App Engine in 2008 which was first public offering for developers.

Over time, these cloud providers kept adding more resources and improving performance of their services to be more market-competitive compared to other providers. There were also providers like IBM, Alibaba, Oracle which came out later in the history. However, AWS, Microsoft and Google remains the three most popular cloud service providers till date.


## Services models

- PaaS
- Iaas
- Saas
- Faas

### cloud models

- Public Cloud: over the public internet by third party provider like Google, MS, AWS, Alibaba
- Multi Cloud: public cloud can be connected with other cloud provider. 
- Hybrid cloud: onprem connected with public cloud. Use cases like disaster recovery, to prevent vendor lock-in. downfall is infrastructure cannot be fully utilized as they have their own proprietary resources. 
- Private Cloud: architecture that exists in on-premise with no public access. Each public cloud has private cloud solution possible on private cloud, Anthos, AWS Outposts, Azure Stack are examples.
