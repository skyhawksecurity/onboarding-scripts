
# Cloud Native Protector (CNP) onboarding tools

Radware's Cloud Native Protector (CNP) monitors resources in your AWS Accounts and Azure Tenants and Subscriptions.

# Onboarding options
in here you will find IaC templates which can be used for the onboarding of your cloud accounts
to CNP

## AWS Accounts 
AWS Accounts onboarding requires a Read Only (SecurityAudit, AWSWAFReadOnlyAccess) permissions to the AWS resources, 
this will allow CNP to query your AWS resources for Hardening warnings.

in the process of onboarding of an AWS Account our IaC Template will create the Required IAM role needed for
CNP.

for those purposes we currently provide the following options:

- [Terraform onboarding](./AWS%20onboarding%20scripts/terraform/)
- [Cloudformation onboarding](./AWS%20onboarding%20scripts/cloudformation/)

## Azure Subscriptions 
Azure Subscription onboarding requires a Read Only (Directory.Read.All, Microsoft.Network/networkWatchers/queryFlowLogStatus/action) permission to the Azure resources, this will allow CNP to query your Azure resources for Hardening warnings.

in the process of onboarding of an Azure Subscription our IaC Template will create the Required Application in Azure AD, attach it to the require service principal and produce a secret for CNP to use, we will also create the required Azure RM Custom Role.

for those purposes we currently provide the following options:

- [Terraform onboarding](./Azure%20onboarding%20scripts/terraform/)