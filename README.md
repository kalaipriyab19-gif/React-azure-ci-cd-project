# React App CI/CD with Azure DevOps (Blue-Green Deployment)

## Overview
This project demonstrates a complete CI/CD pipeline using Azure DevOps to deploy a React application to Azure App Service using Blue-Green deployment strategy.

## Tech Stack
- React
- Azure DevOps
- Azure App Service (Linux)
- Azure Deployment Slots
- YAML Pipeline

## Blue-Green Deployment Flow
1. Code pushed to GitHub
2. Azure DevOps pipeline triggered
3. React app is built
4. App is deployed to the staging slot
5. Staging slot is swapped with production
6. Zero downtime deployment achieved

## Pipeline Stages
### Build Stage
- Install npm dependencies
- Build React application
- Publish build artifacts

### Deploy Stage
- Deploy build to Azure App Service staging slot
- Swap staging slot with production

## Rollback Strategy
If an issue occurs after deployment:
- Swap the slots back from Azure Portal
- No redeployment required

## Outcome
- Zero downtime deployment
- Fast rollback
- Production-safe releases
