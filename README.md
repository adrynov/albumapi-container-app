# Azure Container Apps - Album API

https://learn.microsoft.com/en-us/azure/container-apps/tutorial-code-to-cloud?tabs=bash%2Ccsharp&pivots=docker-local


install or update the Azure Container Apps extension for the CLI:

```sh
az extension add --name containerapp --upgrade --allow-preview true
az provider register --namespace Microsoft.App
az provider register --namespace Microsoft.OperationalInsights
```

Create variables:

```sh
export RESOURCE_GROUP="mslearn"
export LOCATION="northeurope"
export ENVIRONMENT="mslearn-containers-env"
export API_NAME="mslearn-music-api"
export FRONTEND_NAME="mslearn-album-ui"

export GITHUB_USERNAME="adrynov"
export ACR_NAME=$GITHUB_USERNAME
```


export API_BASE_URL=$(az containerapp show --resource-group $RESOURCE_GROUP --name $API_NAME --query properties.configuration.ingress.fqdn -o tsv)
