Web App Log Retrieval
====

You can retrieve the logs from your individual InRule App Service Web Apps via the Azure CLI.

## Sign in to Azure
First, [open a PowerShell prompt](https://docs.microsoft.com/en-us/powershell/scripting/setup/starting-windows-powershell) and use the Azure CLI to [sign in](https://docs.microsoft.com/en-us/cli/azure/authenticate-azure-cli) to your Azure subscription:
```powershell
az login
```

## Set active subscription
If your Azure account has access to multiple subscriptions, you will need to [set your active subscription](https://docs.microsoft.com/en-us/cli/azure/account#az-account-set) to where you create your Azure resources:
```powershell
# Example: az account set --subscription "Contoso Subscription 1"
az account set --subscription SUBSCRIPTION_NAME
```

## Retrieve logs from desired Web App
Retrieve a zip file of logs from a specified Web App with the [az webapp log download](https://docs.microsoft.com/en-us/cli/azure/webapp/log?view=azure-cli-latest#az-webapp-log-download) command:
```powershell
# Example az webapp log download --name contoso-catalog-prod-wa --resource-group inrule-prod-rg
az webapp log download --name WEB_APP_NAME --resource-group RESOURCE_GROUP
```
