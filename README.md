# Milvus Vector Database on Azure Cloud

<img src="./img/milvus-horizontal-color.png" width="420" height="240" />
<img src="./img/Azure.png width="420" height="240" >

This project combines the power of the Milvus Vector Database with the Microsoft Azure Cloud
allowing you to bring Vector Search and Embeddings storage to your AI products. 

# Getting started
You have several options for how to get Milvus running on Azure:
- [Azure Container Instance](Azure-Container-Instances/README.md)
- [Azure Kubernetes Service](Azure-Kubernetes-svc/README.md)
- [Milvus Container in Docker](Local-Docker-Deployment/README.md)

## Prerequisites

To get started, users will need access to an Azure subscription.

To deploy using the Deploy to Azure button which leverages an ARM template, you need write access on the resources you're deploying and access to all operations on the Microsoft.Resources/deployments resource type.

## Installation

**Azure Container Instances**

To deploy Milvus to an Azure Container Instance with Azure Volume, go to the `Azure-Container-Instances` folder and follow instructions in the `README.md` to deploy to the Azure Container Instances (ACI) service.

Additionally, you can deploy using the **Deploy to Azure button** below. 

If using the **Deploy to Azure button**, this setup a storage account in Azure for you. Please ensure you have permissions for Azure Container Services and Azure Storage Accounts.

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure-Samples%2Fqdrant-azure%2Fmain%2FAzure-Container-Instances%2FARM-templates%2Fqdrant-deploy-aci-linkedstorage-params.json)

**Azure Kubernetes Service**

To deploy Milvus to a cluster running in Azure Kubernetes Services, go to the `Azure-Kubernetes-Svc` folder and follow instructions in the `README.md` to deploy to a Kubernetes cluster with Load Balancer on Azure Kubernetes Services (AKS). 

You can quickly create an **Azure Kubernetes Service** cluster by clicking the Deploy to Azure button below. After creating your AKS cluster, go to the `Azure-Kubernetes-Svc` folder to deploy **Milvus** into the AKS cluster using **Helm**.

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure-Samples%2FMilvus-azure%2Fmain%2FAzure-Kubernetes-Svc%2Faks-arm-deploy.json)


**Docker (Local)**

To run the **Milvus** vector database running in **Docker** locally, please follow the instructions from Milvus's website: 
[Install Milvus with Docker](https://milvus.io/docs/install_standalone-docker.md)

To run Milvus with Docker locally, you can use the following command using the docker file stored `docker-compose.yml` located in the `Local-Docker-Deployment` folder. 

In same directory as the `docker-compose.yml` file, run the following command:
```bash
sudo docker-compose up -d
```
In order to check if the containers are running successfully, run the following command:
```bash
sudo docker-compose ps
```

## Resources for Learning More
- Milvus Vector Search (Vector Database): https://milvus.io/
- Milvus Integration with OpenAI: https://zilliz.com/blog/how-to-integrate-openai-embedding-api-with-zilliz-cloud 
- Azure Container Instances (ACI): https://learn.microsoft.com/en-us/azure/container-instances/
- Azure Kubernetes Service (AKS): https://learn.microsoft.com/en-us/azure/aks/
- Docker Desktop: https://docs.docker.com/desktop/ 
