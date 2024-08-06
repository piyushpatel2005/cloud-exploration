# Resource Hierarchy

Google cloud resources are the computing and storage services that you use from GCP for your business. Knowing how these resources are organized is very important in order to describe functionalities of each of them. They are also very important to know because permissions are inherited based on where permissions are assigned in the resource hierarchy.

## What is a Resource?

Service level resources used to process your requests. Compute Engine Instances, Cloud Storage buckets, Cloud SQL databases.
Account level resources like Organization, Folders, Projects.

Resource hierarchy is Google Cloud's way of configuring and granding access to various google cloud resources at service level as well as account level. This can define granular permissions needed for your resources.

Cloud resources are organized hierrachical using parent/child relationshiup.
desinged to map organizational structure to Google cloud
provides better management of permissions and access control
accessibility or permissions are managed by policies controlled by IAM
IAM policy is set on a parent, the child will inherit policies by default.
Access control policies and configuration settings on a parent resource are inherited by the child.
Each child project can have exactly one parent.

At the top we have domain or cloud level. Primary identity of organization. This is where users, policies are defined linekd to Gsuite or identity
Below is organization level. linked to domain. Is the root node of resource hierarchy. exactly associated with one domain. All control policies applied to organization are applied to any layer below it like folders, projects.
When organization is created  organization admin is created. 
Folders layer is to additional grouping layer. A folder can have other folders or projects. like teams and products. A folder can have exactly one parent.
Projects are core organizational component. base level organizing entity. Any given resource can exist in only one project
Resources are service level resource created in google cloud: compute engine instances, Cloud SQL databases, APIs, users,

Labels help categorize resources by key-value pairs. attach to any resource. organize costs when comes to billing. Everything under domain domain till project is account level resource and everything below project level is considererd service-level resource.

how policies applied in hierarchical manner