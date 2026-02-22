# Create IAM User

In earlier lesson, I mentioned you should never use root user for your day to day activity. We hardened that credentials by adding MFA access token, but those credentials should not be used for your daily interaction with AWS. Generally, for each employee or user of your AWS account, you will have a separate IAM user created and assigned to that user. Here, IAM stands for Identity and Access Management which is a central service which manages Authentication and Authorization for all services in your AWS account. If your root user credentials are compromised, there is no way you can restrict what that user can do. This is the primary reason to avoid using that account. If the same thing happens with any of the IAM users, you can still use your root credentials and restrict the permissions of the IAM user which is compromised and potentially save your business.

Every AWS account has an IAM service which is specific to that AWS account. The users/groups or permissions in one account are not accessible to another account. It's totally isolated across AWS accounts. IAM is a globally resilient service which means data is secure across AWS regions. In IAM, you can create different kinds of identities which includes users, groups, and roles. Each of these identities have their own purposes. IAM is used to manage these identities, that is to create, update or delete these identities in your AWS account.

- **Users:** These are human users or applications which need access to some AWS account resources. For example, if John needs access to only S3 Read permission, you can assign John with that permission alone and nothing else.
- **Groups:** Groups are colelctions of related users. For example, you can group for development, infrastructure and finance teams. Each of these groups will have separate set of permissions and any new developer joining the development team can be easily added to the development group and that new user will inherit the permissions assigned to the development group. You will not have to assign permissions individually to each user everytime a new user joins the team. This helps better organize your permissions.
- **Roles:** The roles can be used by AWS services. This can be useful when you want one service to be able to do something with another service. 

Ther is also IAM **policy** documents which are simply JSON documents representing what services or actions allowed or denied on a specific service. These policy documents are attached to one of the identities mentioned above in order for them to be able to perform certain action. IAM authenticates an identity which is to prove what you claim to be and authorizes them to perform certain actions based on policy documents attached to that identity.

You will learn more about these in the IAM section of the lessons.

## Create IAM Admin User

Next, we are going to create an IAM user which will be used throughout these lessons to access AWS account and to perform usual operations.

First of all, navigate to IAM service by searching for IAM in the searchbar at the top and clicking on **IAM**.