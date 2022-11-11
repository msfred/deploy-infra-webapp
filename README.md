# Composite Action: deploy-infra-web

A composite action to deploy infrastructure to Azure using ARM or Bicep templates and then deploy an application to an Azure Web App

## Inputs
- azureClientId
- azureSubscriptionId
- azureTenantId
- deploymentSlotName
- environmentId
- location

## Outputs
- resourceGroupName
- webAppName

## Usage
```
- uses: msfred/deploy-infra-webapp@main
  with:
    azureClientId: ${{ secrets.AZURE_CLIENT_ID }}
    azureSubscriptionId: ${{ secrets.AZURE_SUBSCRIPTION_ID }}
    azureTenantId: ${{ secrets.AZURE_TENANT_ID }}
    environmentId: dev
    location: ${{ env.location }}
```
