
```
title: Getting Started
Next:
prev:
```
# Chapter 2: Getting Started with Azure Function Apps

## 2.1 Setting Up Azure Account
Before you can start building and deploying Azure Function Apps, you'll need an Azure account. If you don't have one already, you can sign up for a free Azure account at [azure.microsoft.com](https://azure.microsoft.com/).

## 2.2 Creating a Function App
### 2.2.1 Using Azure Portal
Once you have an Azure account, you can create a new Function App using the Azure portal or command-line tools. Follow these steps to create your first Function App:
1. **Sign in to the Azure portal:** Navigate to [portal.azure.com](https://portal.azure.com/) and sign in with your Azure account credentials.
2. **Create a new Function App:** Click on the "Create a resource" button (+) in the Azure portal, search for "Function App", and then click "Create" to start the creation process.
3. **Configure Function App settings:** Provide a unique name for your Function App, select your preferred subscription, resource group, and hosting plan. You can choose between the Consumption plan (pay-per-use) or the App Service plan (dedicated resources).
4. **Choose runtime stack:** Select the runtime stack for your Function App. Azure supports multiple programming languages including C#, JavaScript, Python, and PowerShell.
5. **Review and create:** Review your settings and click "Create" to provision the Function App.

## 2.3 Writing Your First Function
Once your Function App is created, you can start writing your first function. Azure provides a built-in code editor directly within the portal, or you can develop functions locally using your preferred development environment. Follow these steps to write and deploy your first function:
1. **Navigate to Function App:** In the Azure portal, navigate to your newly created Function App.
2. **Create a new function:** Click on the "Functions" menu on the left sidebar, then click the "Add" button to create a new function.
3. **Choose a template:** Azure provides several function templates to choose from, including HTTP trigger, Timer trigger, Queue trigger, and more. Select the template that best fits your use case.
4. **Write function code:** Write your function code using the programming language and framework of your choice. For example, if you selected the HTTP trigger template, you can write code to handle incoming HTTP requests.
5. **Test locally:** Test your function locally to ensure it behaves as expected. You can use tools like Azure Functions Core Tools or Visual Studio Code for local development and testing.
6. **Publish function:** Once your function is ready, publish it to your Azure Function App using the Azure portal or command-line tools. Azure will deploy your function to the cloud and make it available for invocation.

## 2.4 Triggering Functions
Functions in Azure can be triggered by various events or triggers such as HTTP requests, timer schedules, message queue messages, file uploads, and more. Each function must specify a trigger that determines when the function should execute. Here are some common triggers used in Azure Function Apps:
- **HTTP Trigger:** Executes the function in response to HTTP requests.
- **Timer Trigger:** Executes the function on a pre-defined schedule or time interval.
- **Queue Trigger:** Executes the function when a new message is added to a message queue.
- **Blob Trigger:** Executes the function when a new blob is added or modified in Azure Blob Storage.
- **Event Grid Trigger:** Executes the function in response to events from Azure Event Grid.
- **Service Bus Trigger:** Executes the function when a new message is received on a Service Bus queue or topic.

In the next chapter, we'll dive deeper into writing and configuring functions for different triggers, and explore advanced features and scenarios for Azure Function Apps.
