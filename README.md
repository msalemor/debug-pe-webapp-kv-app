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

## Verify Networking settings

- The Private Endpoint should show up under ```Private endpoint connections```
- There should be no whitelisted IPs if you have selected networks

## Verify Connectivity to WebApp via Private Endpoint

- From the VM in Azure run:
- ```Test-NetConnection -Port 443 pedemoapi.azurewebsites.net```
- Expected Response:
- 

### Verify Connectionvity to the Key Vault via private Endpoint


- From the VM in Azure run:
- ```Test-NetConnection -Port 443 kv-pedemodemo-eus.vault.azure.net```
- Expected Response:
- 
