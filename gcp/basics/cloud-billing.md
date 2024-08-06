# Cloud Billing

What I will cover
create ,edit and delete billing aaccounts

## Billing account and Payments profile

Billing account: cloud level resource managed in console. defines who pays for resources
tracks all costs incurred by gcp usage
linked to payments profile which includes payment methods
can be linked to one or more projects 
also has billing specific roles nad permissions to control access for billling related functions by IAM

available as Self- service option or invoived payments options (offline)
Self-serve: credit or debit card, charged automatically to the payment method
Invoice: must be eligible for this method, cheque or wire transfer, sent by mail or electronically
    Subaccounts: good for resellers to represent your customers. allow to group charges for projects together and linked back to master biling account. Allows for customer separation and ownership.
billing account can pay for projects that is in a different organization
Projects that are not linked to a billing account will have limtied set of services like free services.

Payments Profile:

Google level resource. processes payments for all google services and not just cloud
connects all google services
stores information like name, address
stores payment methods like debit, credit 
single pane of glass for viewing invoices and payments history
controls who can view and receive invoices for your cloud products

two types of payment profiles: individual or business - These cannot be changed. Business gives flexibility to add new users to business profile so that who can view information. Once profile type selected, cannot be changed.

## Demo

Create, edit and close the billing account
- IAM > Roles -> Filter by billing

Blling Account Administrator
Billing Account Creator
User
Viewer
ProjecT Billing Manager:

Owner has full access to all resources

Go to Billing  
Go to account Management. You can renamed and see projects linkedto this biling account
Go to manage billing account, it will show your billing account
You can cclick Create Billing Account > Choose payments profile and Submit and Enable Billing

Click on hamber menu and change biling account > Set account

To close billing account, you would need to unlink the project. So, unlink it,
Go to Account Management > Close billing Account

## Costs and Budget Alerts

### Committed Use Discount

provide discounted prices for your commitment for speciified term.
- ideal for workload with predictable usage needs
- 1 or 3 year period
they are spend based and resource based 
commitment is billed monthly

#### Spend Based commitment

- you spend a minimum amount for a service in a particular region for a year or 3 year
you get discounted rate in response
- Any overage is charged as on-demand rate
- can give you 25% for 1 year and upto 52% discount on a 3 year commitment
- available for cloud sql databasae and Cloud VMware engine. 
- applies only to CPU and memory usage

#### Resource based commitment

- discount for a commitment to spend a minimum amount for comute engine resources in a particular region.
- this is ideal for predictable workload.
- available for vCPU, memory, GPU and local SSDs
- purchase this at discounted rate for committing for 1 or 3 years.
- discount upto 57% for most resource
- discount is upto 70% for mmeory optimied machine types
- can use for single project or across multiple projects
- sharing discount across projects maximizes your discount savings by pooling all resources across projects
- multiple projects sharing same biling account can share committed discounts.

#### Sustained-Use discount

these are automatic discounts for running specific compute engine resources for significant portion of month
- applies to general purpose, machine types
applies to vCPUS and memory for most compute engines
- no action required on your part
- for example, when running one of these resources for more than 25% of month, you get discount
- VMs created by kuberentes egine and compute engine but not to app engine flexible machines  dataflow and e2 machine type
- don't apply to pre-emptible machine types
- can save max upto 30% discount

### GCP Pricing Calculator

a way to calculate your GCP cloud billing cost. This is quick way to get an estimate of what your usage will cost on GCP.
can help you identify pricing for the resources you plan to use in your architecture.
you can calculate your architecture cost.
you can get good idea of your architecture cost.
this calculator can be found at this url.

## Billing Budgets

track your actual spend vs spend plans.
- you can also send budget alerts to send notification once you exceed specific amount or specific portion of your planned spend.
This helps you stay in your budgets
- it is default sent to billing admin
- you can define the scope of the budget. you can scope budget to entire billing account, project or specific resources.
- budget alerts can be set on specific total or based on previous month's spend amount.
- alertemails are sent to billing account admins and users on target cloud account
- email receipients can be customized by using Cloud monitoring to specify other people to receive budget alert emails.
- a project manager, directory or team

- can also use pubsub for programmatic notifications or to automate cost management tasks.
- can provide real-time status of cloud billing alerts
- can help send notifications to slack or pagerduty etc.