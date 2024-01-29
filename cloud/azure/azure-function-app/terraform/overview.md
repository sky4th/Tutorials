```
title: overview
Next:
prev:
```
# Chapter 2.1: Deployement using Terraform 

## Let's deploy a function app  **Using docker Image**. 
## Resources required are
## 1. Storage Account
- Function App Storage: Azure Function Apps use a Storage Account to store various types of data, including execution logs, application settings, and temporary files. This storage is essential for the functioning of the app.

- Triggers and Bindings: Function Apps often use triggers and bindings to interact with external resources like Azure Blob Storage, Azure Queue Storage, or Azure Table Storage. These triggers and bindings require access to a Storage Account for configuration and operation.

- Durable Functions: Durable Functions, an extension of Azure Functions, rely heavily on Azure Storage for managing orchestration state and managing durable entities. A Storage Account is required to support the underlying storage requirements of Durable Functions.

- Dependency Injection: Some applications deployed as Function Apps might require access to external data or resources stored in a Storage Account. This could include configuration files, data files, or any other resources needed by the application.

- Logging and Monitoring: Azure Function Apps generate logs and metrics during execution, which are often stored in a Storage Account for later analysis and monitoring. This helps developers and administrators understand the behavior and performance of their function apps.

- Overall, a Storage Account is a fundamental component in the Azure ecosystem, and Function Apps often leverage its capabilities for various purposes, including data storage, trigger mechanisms, state management, and logging.
2. keyvault and keyvault access policy
Azure Key Vault can be used with Azure Function Apps to securely store and manage sensitive information such as connection strings, API keys, passwords, and certificates. Here's how Key Vault can be used with Function Apps:

Secrets Management: Azure Function Apps can retrieve secrets stored in Azure Key Vault during runtime. This allows you to store sensitive information separately from your code and configuration files, reducing the risk of exposure.

Secure Configuration: Instead of hardcoding sensitive information directly into your function app's code or configuration files, you can reference the secrets stored in Key Vault. This improves security by ensuring that sensitive data is not exposed in plaintext.

Integration: Azure Function Apps can easily integrate with Azure Key Vault using managed identities or service principals. Managed identities allow Function Apps to authenticate with Key Vault without needing to manage explicit credentials.

Access Control: Azure Key Vault provides granular access control, allowing you to define who can read, write, and manage secrets stored in the vault. This ensures that only authorized users and applications can access sensitive information.

Automatic Rotation: Key Vault supports automatic rotation of secrets, allowing you to periodically update sensitive information without modifying your function app's code. This helps improve security by reducing the risk of using stale or compromised credentials.

Audit Logging: Azure Key Vault logs all access and management operations, providing detailed audit trails for compliance and security purposes. This allows you to track who accessed or modified secrets stored in the vault.

Overall, leveraging Azure Key Vault with Azure Function Apps helps improve security, simplify secrets management, and ensure compliance with regulatory requirements by securely storing and managing sensitive information.
3. Private Endpoint

4. Role Assignment
5. Azure Function App Settings

Azure Function App settings are configurations that control various aspects of your function app's behavior and execution environment. These settings can be managed through the Azure portal, Azure CLI, or ARM templates. Here's a brief overview of some common function app settings:

1. Application Settings

These settings include configurations such as connection strings, app settings, and environment variables. They are used to store sensitive information like database connection strings or API keys securely.

2. Runtime Settings

Runtime settings define the execution environment for your function app, such as the version of the runtime stack (e.g., Node.js, .NET, Python) and the version of the Azure Functions runtime.

3. Scaling Settings

Scaling settings control how your function app scales to handle incoming requests. This includes options like manual scaling, auto-scaling based on metrics like CPU usage or queue length, and setting maximum and minimum instances.

4. Monitoring Settings

Monitoring settings enable logging and monitoring features for your function app. You can configure diagnostic logs to be stored in Azure Storage or sent to Azure Monitor for analysis and alerting.

5. Authentication / Authorization Settings

These settings allow you to configure authentication and authorization for your function app, such as enabling authentication with Azure Active Directory (AAD) or setting up OAuth providers like Azure AD, Facebook, or Google.

6. Networking Settings

Networking settings control how your function app communicates with other Azure services and the internet. This includes configuring virtual network integration, IP restrictions, and enabling private endpoints.

7. Advanced Settings

Advanced settings include additional configurations such as CORS (Cross-Origin Resource Sharing) settings, proxy configurations, and managed identity settings for accessing other Azure resources securely.

By configuring these settings appropriately, you can ensure that your Azure Function App operates efficiently, securely, and in alignment with your application requirements.
