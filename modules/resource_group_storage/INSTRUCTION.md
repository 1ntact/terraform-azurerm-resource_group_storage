# Terraform Azure Resource Group Storage Module

## Description

This Terraform module creates an Azure Resource Group and Storage Account.

## Requirements

Before using this module, make sure you have:

* Terraform installed
* An active Azure subscription
* Azure CLI installed and authenticated
* AzureRM Terraform provider configured

## Usage

Add the module to your Terraform configuration:

```hcl
module "resource_group_storage" {
  source = "github.com/YOUR_USERNAME/terraform-azurerm-resource_group_storage"

  resource_group_name  = "example-resource-group"
  location             = "West Europe"
  storage_account_name = "examplestorage123"
}
```

Replace `YOUR_USERNAME` with your GitHub username.

## Inputs

| Name                       | Description                                  | Type     | Default    | Required |
| -------------------------- | -------------------------------------------- | -------- | ---------- | -------- |
| `resource_group_name`      | Name of the Azure Resource Group             | `string` | -          | Yes      |
| `location`                 | Azure region where resources will be created | `string` | -          | Yes      |
| `storage_account_name`     | Name of the Azure Storage Account            | `string` | -          | Yes      |
| `account_tier`             | Storage Account performance tier             | `string` | `Standard` | No       |
| `account_replication_type` | Storage Account replication type             | `string` | `LRS`      | No       |

## Outputs

| Name                   | Description                         |
| ---------------------- | ----------------------------------- |
| `resource_group_name`  | Name of the created Resource Group  |
| `resource_group_id`    | ID of the created Resource Group    |
| `storage_account_name` | Name of the created Storage Account |
| `storage_account_id`   | ID of the created Storage Account   |

## Terraform Commands

Initialize the Terraform configuration:

```bash
terraform init
```

Validate the configuration:

```bash
terraform validate
```

Create an execution plan:

```bash
terraform plan
```

Apply the configuration:

```bash
terraform apply
```

Destroy the created resources:

```bash
terraform destroy
```

## Module Structure

```text
terraform-azurerm-resource_group_storage/
├── main.tf
├── variables.tf
├── outputs.tf
├── INSTRUCTION.md
├── LICENSE
└── .gitignore
```

## License

This module is distributed under the MIT License.
