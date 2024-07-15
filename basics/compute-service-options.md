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

- function as a services. serverless execution enrivonment for building and connecting various cloud services.
single function with focus on specific events.
triggered when event is fired
no need to manage infrastructure
written using Java, Python, Go languages
good choice for data processing or event based triggers
web hooks for responding to HTTP triggeres
mobile backend
loosely coupled logic for APIs.

### cloud Run

fully managed compute for deploying and scaling containerized applications
build on open source Knative
abstracts away infra management depending on traffic.
abstract infrastructure - serverless for containers
flexibility for language, binary or library. considered Faas

more flexiblity at top and less flexibility on cloud run (bottom)