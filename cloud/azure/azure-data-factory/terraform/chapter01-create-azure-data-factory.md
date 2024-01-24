```
title:- Create Azure Data Factory
author:- Vinod Seth
Next:-
Prev:-
```
# Quickstart: Create an Azure Data Factory
This quickstart describes how to use Terraform to create an Azure data factory. 
## Files
1. main.tf:- this file will contain code for creating ADF and other resource creation code
2. variables.tf:- this file will declare variables required by resources
3. output.tf:- define all output variables which can be used in calling code.
4. provider.tf:- define provider block
5. terraform.tfvars:- provide input variable values

## main.tf
First step is to get the resource group in which you want to create data factory
1. get the resource group
```terraform
data "azurerm_resource_group" "main" {
  name = var.resource_group_name
}
```
2. create Azure Data Factory
Now lets Azure Data Factory in resource group fetched above.
```terraform
resource "azurerm_data_factory" "data_factory" {
  location                        = data.azurerm_resource_group.main.location
  name                            = var.adf_name
  resource_group_name             = data.azurerm_resource_group.main.name
  public_network_enabled          = var.public_network_enabled
  managed_virtual_network_enabled = true
  tags                            = merge(var.tags, local.required_tags)

  # Ignore changes to tags
  lifecycle {
    ignore_changes = [
      tags,
      vsts_configuration,
      global_parameter
    ]
  }

}
```
## variables.tf
Lets decalre varibles
```
variable "resource_group_name" {
  description = "(Required) The resource group where this resource will be provisioned"
  type        = string
}

variable "adf_name" {
  description = "(Required) The name of the ADF"
  type        = string
}
variable "tags" {
  description = "Tags associated with this resource"
  type        = map(string)
  default     = {}
}
variable "public_network_enabled" {
  description = "Is the Data Factory visible to the public network? Defaults to true"
  type        = bool
  default     = false
}
```
## outputs.tf
lets decalre output vaiables
```
output "id" {
  value = azurerm_data_factory.data_factory.id
}

output "name" {
  description = "Name of the data factory"
  value       = azurerm_data_factory.data_factory.name
}
```
## provider.tf
if you are using terraform cloud, add below code
```
terraform {
# cloud block is required if are using terraform cloud. if you are not using terraorm cloud then delete cloud block
  cloud {
    organization = "your organisation name"

    workspaces {
      name = "your workspace name"
    }
  }

required_providers {
    azurerm = {
      source  = "hashicorp/azurerm"
      version = ">=3.7.0"
    }
  }
}
provider "azurerm" {
  features {}
  skip_provider_registration = true
}  
```
## terraform.tfvars
```
resource_group_name = <provide reqource group name> # mandatory
adf_name = <provide adf name> # mandatory
public_network_enabled = <provide value> # optional
tags = <provide tags as key-value pair> # optional
```
Terraform code is eady to be deployed now.

# Steps to deploy
1. run "terraform init"
2. run "terraform plan". Analyse the plan output carefully if it matches exactly with your expectaion then go ahead with next step
3. run "terraform apply"

<b>Note:- this will create terraform state file locally or in terraform cloud workspace, if have used cloud block in provide.tf</b>

 If code executes successfully , go to Azure portal and verify whether azure data factory has been created. if yes thats great, <b>you have successfully created Azure Data factory.</b>
 But thats just begining as we have only created ADF but its not doing anything useful.
 lets Move to next session to make more meaningfull
 
 [ADF Data source and sink](https:/)

