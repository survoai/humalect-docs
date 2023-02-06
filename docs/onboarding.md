---
sidebar_position: 4
---

# Onboarding on the Humalect platform

Following are the steps to host your infrastructure and deploy your applications using the Humalect platform.

1. [Signup with humalect](https://docs.humalect.com/en/platform/onboarding#signup-with-humalect) - If you are reading this, then chances are that you already have the login details
2. [Integrate your Cloud Provider](https://docs.humalect.com/en/platform/onboarding#integrate-your-cloud-provider)
3. [Integrate your Source Code Provider](https://docs.humalect.com/en/platform/onboarding#integrate-your-source-code-provider)
4. [Create a Kubernetes Cluster](https://docs.humalect.com/en/platform/onboarding#create-a-kubernetes-cluster)
5. [Create the Desired Environments](https://docs.humalect.com/en/platform/onboarding#create-the-desired-environments)
6. [Create Data Sources (optional)](https://docs.humalect.com/en/platform/onboarding#create-data-sources-optional)
7. [Create Projects](https://docs.humalect.com/en/platform/onboarding#create-projects)
8. [Create Pipelines](https://docs.humalect.com/en/platform/onboarding#create-pipelines)
9. [Start Shipping code](https://docs.humalect.com/en/platform/onboarding#start-shipping-code)


---
## Signup with humalect
You need to get the access to login by signing up with humalect. There are 2 ways to signup with Humalect which are discussed [here](https://docs.humalect.com/en/platform/signup).

---
## Integrate your Cloud Provider

You need to connect your cloud provider with Humalect so that we can seemlessly ship your deployments and commits. We take minimal permissions for the connected cloud account. Currently we support only AWS and Azure cloud platforms. In order to connect with them you can visit the following documentation links.
1. [Integrating AWS with Humalect](https://docs.humalect.com/en/Cluster/cluster-aws)
2. [Integrating Azure with Humalect](https://docs.humalect.com/en/Cluster/cluster-azure)

---
## Integrate your Source Code Provider

We need to integrate with your Source Code Provider to automatically build your commits and provide you with options to run various environments from your source code repositories and their branches. Currently, we support only Gitlab, Github and Bitbucket. In order to connect with bitbucket, you can visit  [Integrating Bitbucket with Humalect](https://docs.humalect.com/en/integrations/bitbucket).
<!-- TODO
2. [Integrating Gitlab with Humalect](https://docs.humalect.com/en/integrations/bitbucket).
3. [Integrating Github with Humalect](https://docs.humalect.com/en/integrations/bitbucket). -->
In order to connect Github and Gitlab, you can visit https://console.humalect.com/user/integrations and follow their respective workflows.

---
## Create a Kubernetes Cluster
To host your deployments, we will need a kubernetes cluster that will have the respective deployments, services and ingress. We have got you covered with that as well. You just need to follow few steps mentioned in the doc linked below with respect to your cloud provider and your Kubernetes cluster is good to go.

1. [Creating an AWS cluster with Humalect](https://docs.humalect.com/en/Cluster/cluster-aws).

2. [Creating an Azure cluster with Humalect](https://docs.humalect.com/en/Cluster/cluster-azure).


---
## Create the Desired Environments
You might need multiple environments such as staging, development and production. Humalect platform uses kubernetes namescapes to host your environments.  
To learn more about how to create environments, please visit https://docs.humalect.com/en/EnvironmentPage .


---
## Create Data Sources (optional)
Humalect Datasources allow you to deploy your choice of databases/caches in your kubernetes cluster in a few clicks. The data is safely stored in persistence volumes with your cloud provider. We currently support Redis, MongoDB and Postgres.
Visit the links below for instructions on how to create your databases.

1. [Creating Redis with Humalect](https://docs.humalect.com/en/DataSources/Redis)
2. [Creating MongoDB with Humalect](https://docs.humalect.com/en/DataSources/MongoDB)
3. [Creating PostgreSQL with Humalect](https://docs.humalect.com/en/DataSources/Postgres)
---
## Create Projects
We need a logical mapping between source code repositories and cluster on which they will be deployed. We call it Projects in the Humalect universe.
To learn more about how to create the Projects, please visit  https://docs.humalect.com/en/project

---
## Create Pipelines
Pipelines act as a source of truth for all your deployments as they encompass every detail related to them like YAMLs, Dockerfile, port number, sub-domain etc.

To learn more about how to create the Pipelines, please visit https://docs.humalect.com/en/CreatingPipeline


---
## Start Shipping code
Once you are done creating your pipleline, there are two ways to deploy your code:
1. **Manually deploying the pipeline** -> Visit the respective pipeline detail page and then press the Deploy button to deploy the pipeline.
2. **Automatically deploying the pipeline using CD** -> If you have checked the `CD enabled` box while creating your pipeline, all your future commits will be automatically deployed.

You have now onboarded successfully on the Humalect platform. Do reach out to us for questions and feedback!
