---
sidebar_position: 4
---

# Onboarding on the Humalect platform

Following are the steps to host your infrastructure and deploy your applications using the Humalect platform.

## Signup with humalect

visit https://humalect.com and sign up. Complete the registration flow and log in

---
## Integrate your Cloud Provider

You need to connect your cloud provider with Humalect so that we can seamlessly ship your deployments and commits. Currently we support only AWS and Azure cloud platforms. In order to connect AWS and Azure, you can visit [this link](https://console.humalect.com/user/integrations) and follow their respective workflows.

---
## Integrate your Source Code Provider

We need to integrate with your Source Code Provider to automatically build your commits and provide you with options to run various environments from your source code repositories and their branches. Currently, we support Gitlab, GitHub and Bitbucket. In order to connect with Bitbucket, you can visit [Integrating Bitbucket with Humalect](./../docs/Integrations/Bitbucket).
<!-- TODO
2. [Integrating Gitlab with Humalect](to-be-added).
3. [Integrating Github with Humalect](to-be-added). -->
In order to connect Github and Gitlab, you can visit [this link](https://console.humalect.com/user/integrations) and follow their respective workflows.

---
## Create a Kubernetes Cluster
To host your deployments, we will need a Kubernetes cluster that will have the respective deployments, services and ingress. We have got you covered with that as well. You just need to follow few steps mentioned in the doc linked below with respect to your cloud provider and your Kubernetes cluster is good to go.

1. [Creating an AWS cluster with Humalect](./../docs/Clusters/create-an-AWS-cluster).

2. [Creating an Azure cluster with Humalect](./../docs/Clusters/create-an-Azure-cluster).


---
## Create the Desired Environments
You might need multiple environments such as staging, development and production. Humalect platform uses Kubernetes namescapes to host your environments. 
To learn more about how to create environments, please visit [environments](./../docs/Environments/Overview)


---
## Create Datasources
Humalect datasources allow you to deploy your choice of databases/caches in your Kubernetes cluster in a few clicks. The data is safely stored in persistence volumes with your cloud provider. We currently support Redis, MongoDB and Postgres.
Visit the links below for instructions on how to create your databases.

1. [Creating Redis with Humalect](./../docs/Datasources/Redis)
2. [Creating MongoDB with Humalect](./../docs/Datasources/MongoDB)
3. [Creating PostgreSQL with Humalect](./../docs/Datasources/Postgres)
---
## Create Projects
We need a logical mapping between source code repositories and cluster on which they will be deployed. We call it Projects in the Humalect universe.
<!-- To learn more about how to create the Projects, please visit [projects](./../docs/projects/overview) -->

---
## Create Pipelines
Pipelines act as a source of truth for all your deployments as they encompass every detail related to them like YAMLs, Dockerfile, port number, sub-domain etc.

To learn more about how to create the Pipelines, please visit [pipelines](./../docs/Pipelines/overview)


---
## Start Shipping code
Once you are done creating your pipeline, there are two ways to deploy your code:
1. **Manually deploying the pipeline** -> Visit the respective pipeline detail page and then press the Deploy button to deploy the pipeline.
2. **Automatically deploying the pipeline using CD** -> If you have checked the `CD enabled` box while creating your pipeline, all your future commits will be automatically deployed.

You have now onboarded successfully on the Humalect platform. Do reach out to us for questions and feedback!

