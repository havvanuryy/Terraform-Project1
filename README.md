# Project1-Terraform 
## Creating  Resource group, Storage account, Virtual machine, and Virtual network

To create a resource group, **rg.tf** file is created. For further details [see](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs).

To create a storage account, **sa.tf** file is created. For further details [see](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_account).

To create virtual machine and virtual network, **vmvnet.tf** file is created. For further details [see](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/virtual_machine).

To define centrally controlled reusable values, **variables.tf** file is created. For further details [see](https://developer.hashicorp.com/terraform/language/values/variables).

After **.tf** files are created, we need to log in to our Azure account.

```
# to log in Azure portal
az login
```

The **terraform init** command initializes a working directory containing Terraform configuration files. 

This is the first command that should be run after writing a new Terraform configuration or cloning an existing one from version control.

It is safe to run this command multiple times. For further information and usage [see](https://developer.hashicorp.com/terraform/cli/commands/init).

```
# to initialize a working directory
terraform init
```

The **terraform plan** command creates an execution plan, letting you preview the changes Terraform plans to make to your infrastructure. 
By default, when Terraform creates a plan it:
 - Reads the current state of any already-existing remote objects to ensure the Terraform state is up-to-date.
 - Compares the current configuration to the prior state and notes any differences.
 - Proposes a set of change actions that should, if applied, make the remote objects match the configuration. 
For further information and usage [see](https://developer.hashicorp.com/terraform/cli/commands/plan).

```
# to create an execution plan
terraform plan
```

The **terraform apply** command executes the actions proposed in a Terraform plan. For further information and usage [see](https://developer.hashicorp.com/terraform/cli/commands/apply).
```
# to execute .tf files
terraform apply
```
Finally, we can log in to Azure Portal and see our resource group and resources in it. Here is an [example](https://github.com/havvanuryy/TerraformProject1/blob/main/AzurePortal_Images.pdf).
