# Compute Service Offering

Google cloud has lots of services available for computations. At one side of the services, we have Compute Engines, which provides lot more flexibility and at the other end, you have choice of Cloud functions in which you simply write a function to perform specific function, giving less flexibility but at the same time, minimal administration.

So, let's first get a brief overview of these services.

### Compute Engine

This is a Iaas offering on GCP where you can create virtual machines. Compute Engines can be deployed in any region or zone. This is a zonal resource so it is always deployed in a single zone. While creating a virtual machine, you can choose from range operating systems offered, CPU, memory, storage and other services you want to run on the VM. You can customize what software run on the compute engine using initialization scripts. There are also customized pre-made instance images in the Google Cloud Marketplace.

VMs can be standard, preemptible or spot instances. Pre-emptible and spot VMs offer 70 - 90% cost savings but those can be evicted anytime when GCP needs resources. You can also manage multiple instances as a part of Instance groups. Instance groups can be managed or unmanaged. With Managed instance groups, you can also auto scale number of instances based on various compute metrics. With compute engine, you have flexibility of attaching persitent disks or you can detach them when you don't need those. These machines can be accessed by SSH for Linux and RDP for windows. You can also set firewall rules to make these instances accessible for only certain IP or range of IP addresses.

###  Kubernetes Engine

Kubernetes is container orchestration service designed to deploy and manage scalable applications. This is build on the same Kubernetes project that Google open sourced in 2014. Due to this, it offers lot more flexibility of integrating with on-prem kubernetes. In kubernetes the resources are created using declarative approach and kubernetes manages the application state based on desired state. It uses compute engine as the backend worker nodes in a kubernetes cluster. A cluster is simply a group of nodes or VMs. This is also known as Container as a service offering on Google Cloud platform.

Anthos extend GKE functionalities for hybrid and multi-cloud environments. It allows same set of functionalities by providing service to create, scale and updatrade Kubernetes clusters along with a common orchestration layer. Multiple clusters can be managed as a group of cluster known as *fleet*. 

### App Engine

App Engine is GCP's Paas offering. In this, developers or SysAdmins don't need to be concerned about the VMs or configuration of Kubernetes cluster, they can simply focus on developing the application. It's a fully managed serverless platform for developing and hosting web application at scale. Google Cloud platform manages the underlying resources for the application and it will automatically scale the resources based on the load. Google is also responsible for managing the security and patching for the infrastructure. App Engine also allows seamless connections with other Google cloud services. App Engine is available in two types:
1. Standard: This is where you can run applications in a language-specific sandbox. It supports only few languages, so developers will have to write the application code in one of the supported languages and there is no control over the infrastructure so additional OS level packages cannot be installed.
2. Flexible: In this mode, the developer runs containerized application in App Engine environment. This runs on containers so there is lot more flexibility in choosing language or it's even possible to install OS specific packages.

### Cloud Functions

Cloud Functions is a lightweight function as a service or Faas offering on GCP. It is a serverless execution environment for building and connecting various cloud services. Users of this service do not need to manage any infrastructure just like App Engine. The basic idea is that you write a single targeted function which executes on a specific event. Cloud functions are associated with an event which acts as a trigger for the function. These are events such as when file is uploaded to storage bucket or a message is published in Pub/Sub topic or other events with the help of Pub/Sub messaging. The function should be small enough to execute in short duration. The code for the function can be writte in one of the supported language runtimes. This is useful for event-based function triggers. Systems like web hooks for responding to HTTP(s) requests or for mobile backend or even ETL processing of asynchronous jobs are well suited to Cloud functions. 

### cloud Run

Cloud Run is a fully managed compute offering for deploying and scaling containerized application on GCP. This is build on top of open source Knative project and is used for running stateless backend applications. This is also considered one of the Paas solutions for container based development.It abstracts away infrastructure management as developers do not have to manage infrastructure or autoscaling of the application. These are built-in to Cloud Run with pay per use model. You can have up to 1000 container instances by default. This being compute for containerized applications, you're not restricted to using only specific programming langauges and also offer flexibility in configuring the underlying operating system packages. 