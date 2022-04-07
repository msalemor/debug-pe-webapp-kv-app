# debug-pe-webapp-kv-app
Debugging an Azure Web App with Azure Key Vault both with Private Endpoints

# Steps to debug

## Resources

- Deploy VNET and Subnets
  - default or higher /245
  - AzureBastionSubnet /24
  - vmSubnet /24
  - peSubnet /24
  - baSubnet /28 or higher
- Deploy Web App (Production SKU with VNET integration)
- Deploy Key Vault
- Create a secret
- Deploy a VM to the vmSubnet
- Enable VNET integration in the Web App and use the baSubnet
- Deploy a Private Endpoint for Web App to the peSubnet
- Deploy a Private Endpoint for Key Vault to the peSubnet

## Verify Private DNS Zones

## Verify Connectivity to WebApp

- From the VM in Azure run:
- ```Test-NetConnection -Port 443 {webappname}.azurewebsites.net```
- Expected Response:
- 

### Web App Connectivy



