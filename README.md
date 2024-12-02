# Azure Container Apps - Album API

https://learn.microsoft.com/en-us/azure/container-apps/tutorial-code-to-cloud?tabs=bash%2Ccsharp&pivots=docker-local


export RESOURCE_GROUP="mslearn"
export LOCATION="northeurope"
export ENVIRONMENT="mslearn-containers-env"
export API_NAME="mslearn-music-api"

export GITHUB_USERNAME="adrynov"

export ACR_NAME="acr"$GITHUB_USERNAME

FRONTEND_NAME="album-ui"

export API_BASE_URL=$(az containerapp show --resource-group $RESOURCE_GROUP --name $API_NAME --query properties.configuration.ingress.fqdn -o tsv)
