# Azure-ARM-Templates
ARM templates for automation of VM creations in Azure Cloud

Open Powershell and connect to your Azure account by runing below command.
-> Connect-AzureRmAccount

Create a resource group and set the location by running below command. Replace 'rsgroup_name' with preferred and comfortable name and Choose the location where you want to deploy the VM.
-> New-AzureRmResourceGroup -Name <rsgroup_name> -Location "<eg. Central US>"

Run the below command to deploy the VM. Replace 'location\Template_file_name.json' with template file path and name.
-> New-AzureRmResourceGroupDeployment -ResourceGroupName rsgroup -TemplateFile <location\Template_file_name.json>

Deployemnt:
-> When it ask for OsType:, Type Windows or Linux based on the kernal of the VM you deploy.
-> Enter the Existing Storage account name.
-> Enter the VNET, Subnet name and range to be created
-> Enter the Size of the VM to be created (Choose it wisely)
	Refer: https://learn.microsoft.com/en-us/azure/templates/microsoft.compute/virtualmachines?pivots=deployment-language-bicep
	-> Enter the name for VM to be created.

