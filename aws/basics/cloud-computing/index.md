# Cloud Computing

Cloud computing is a term used to describe a computing environment where computing resources are provided on demand and on a pay-as-you-go basis. This means organizations do no need to reserve computing resources in advance and they can ask for new resources when they actually need them and they will have those available without pre-planning. These resources can be provided by AWS, Azure, Google Cloud, etc. It is very important these days due to its ability to offer flexible and cost effective computing resources. On top of these, it offers scalability and high availability which are essential for modern day businesses. Organizations can scale their resources up and down depending on the demand of their business.

## Features of Cloud Computing
Cloud computing can be characterized by below features.

- **On-demand**: You can provision new resources whenever you need them and this is done through the internet. You do not need to be physically present at any data center to provision a server.
- **Self-serve**: You can provision the resources using few commands without any intervention of the IT team. 
- **Resource sharing**: The computing resources are shared across multiple different customers using a multi-tenant model. The physical and virtual servers are dynamically assigned to each customer based on demand. This helps in economies of scale.
- **Elastic**: The computing resources are elastic in nature. They can be scaled up when you need more resources and scaled down when demand decreases to reduce costs.
- **Pay-as-You-Go**: Cloud computing uses a pay-as-you-go model. With this model, you're charged only for the services used by the bussiness and not for anything idle.

## Cloud Deployment Models

In order to leverage full benefits of the cloud technology, it's essential to understand the various types of cloud deployment models. These are four types of deployment models: private, public, multi cloud and hybrid cloud.

### Private Cloud

Whenever a business requires technology that can be accessible just inside their own company without public exposure, private cloud might be a possible option. For example, if a company wants to host their intranet website for their employees to be able to collaborate design documents or even documentation, they can use private cloud. In this case, only company employees can access this website.

Interestingly, each public cloud provider also provides a solution to host private cloud solutions such as Google Anthos, Microsoft Azure Stack or AWS Outposts.

### Public Cloud

This is the most common deployment model as most customers move to cloud to use this capability. Any business offering public facing application or website can use public cloud providers to use their services as a public cloud. In this case, they create similar resources but on the public cloud and assign public IPs which can be accessible from anywhere in the world over the internet. Public Cloud services are prone to DDos attacks or other types of hacker or malware attacks. Therefore security is a major concern for any publicly accessible software applications.

### Multi Cloud
Multi cloud deployment model is usually used by large enterprise customers. This provides customers freedom to choose the best service across any of the cloud providers. For example, a customer can choose Google Dataflow for processing large datasets present in S3 bucket as a storage layer. This also avoids possibility of vendor lock-in and customer can choose best pricing per service. For example, Compute Engines might be better priced in GCP whereas databases might be bette priced in Azure or AWS and they can choose relevant services from each of these providers.

### Hybrid Cloud
Hybrid cloud is like a middle layer between on-premises and public cloud. Businesses can deploy internal services and applications within internal network on the private cloud or on-premises whereas public facing services can be deployed in public cloud to provide better availability and scalability. This also provides better security for internal applications with total control over those applications.

## Types of Cloud Computing

You can also choose how you want to run your cloud services using one of the service models. This choice will be based on security, compliance, cost and several other factors. You can run your services fully on-premises, as a IaaS, PaaS or SaaS. Let's see what those are.

### On-Premises

In this mode, the code is deployed on on-premises environment. These are servers purchased or rented with agreement with the data center. There will be special SysOps team to manage these resources and to provision virtual machines on those servers. This is where you will have to pre-plan if you need to extend your infrastructure or if you need to scale up or down. This on the other hand, provides full control over the infrastructure.

### Infrastructure as a Service (IaaS)

In Iaas, a user needs to handle all the service configurations. This also provides lot of control over the infrastructure including computing and networking. However, with more control, the customer is responsible for more responsibility because they will need to manage the networking, computing infrastructure and storage layers etc. All of these require specialized skills which adds to costs of the team. This also means in general, Iaas might be costlier than PaaS or SaaS model. As you can see from above picture that in this case, the customer controls everything in the application stack except the underlying virtualization and the physical server racks in the data center.

Some services provided under IAAS by AWS are IPs, Firewalls, S3, Virtual Private Cloud, and EC2 machines.
### Platform as a Service (PaaS)

Platform as a service, or also known as Paas, delivers and manages all the hardware and software resources to develop applications through the cloud. In this model, developers and IT teams are not fully responsible for managing the infrastructure. The physical hardware, networking and even OS updates are managed by the cloud provider.Developers and IT operations teams can use PaaS to develop, run, and manage applications without having to build and maintain the infrastructure or platform on their own. Customers still have to write the code and manage their data and applications, but the environment to build and deploy apps is managed and maintained by the cloud service provider. 

On AWS, services like AWS Beamstalk, RDS, App Runner, etc. are examples of PaaS services. The customers can provision these resources as they need them and then use them. They are not responsible for managing the physical servers.

### (Software as a Service) Saas
Software as a service, or SaaS, provides the entire application stack over the internet, delivering an entire cloud-based application that customers can access and use. SaaS products are completely managed by the service provider and come ready to use, including all updates, bug fixes, and overall maintenance. Most SaaS applications are accessed directly through a web browser, which means customers don’t have to download or install anything on their devices. They can simply access these services using their web browser.

Services like Gmail, Maps, Salesforce, Snowflake are examples of Saas applications.

There are few other types of computing if you want to be more granular. They can be categorized into Function as a Service (FaaS) or Container as a Service (CaaS).