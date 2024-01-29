```
title: overview
Next:
prev:
```
# Chapter 2.1: Deployement using Terraform 

## 2.1.1 Use case
Lets deploy a function app  **Using docker Image**. the resources required are
1. Storage Account
2. Private Endpoint Subnet
3. Function app settings
3.1 **Application Settings**: These settings include configurations such as connection strings, app settings, and environment variables. They are used to store sensitive information like database connection strings or API keys securely.
3.2 **Runtime Settings**: Runtime settings define the execution environment for your function app, such as the version of the runtime stack (e.g., Node.js, .NET, Python) and the version of the Azure Functions runtime.
3.3 **Scaling Settings**: Scaling settings control how your function app scales to handle incoming requests. This includes options like manual scaling, auto-scaling based on metrics like CPU usage or queue length, and setting maximum and minimum instances.
3.4 **Monitoring Settings**: Monitoring settings enable logging and monitoring features for your function app. You can configure diagnostic logs to be stored in Azure Storage or sent to Azure Monitor for analysis and alerting.
Authentication / Authorization Settings: These settings allow you to configure authentication and authorization for your function app, such as enabling authentication with Azure Active Directory (AAD) or setting up OAuth providers like Azure AD, Facebook, or Google.
3.5 **Networking Settings**: Networking settings control how your function app communicates with other Azure services and the internet. This includes configuring virtual network integration, IP restrictions, and enabling private endpoints.
3.6 **Advanced Settings**: Advanced settings include additional configurations such as CORS (Cross-Origin Resource Sharing) settings, proxy configurations, and managed identity settings for accessing other Azure resources securely.

