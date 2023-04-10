---
slug: /cluster-overview
title: Clusters Overview
description: Easily create Kubernetes clusters in a few clicks
---

## Introduction to Clusters

In Kubernetes, a cluster is a set of machines, called nodes, that are used to run containerized applications. Each node in a Kubernetes cluster runs a container runtime, such as Docker, and is managed by the Kubernetes control plane. The control plane is responsible for scheduling and managing the containers that are running on the nodes.

A Kubernetes cluster typically includes at least one master node and one or more worker nodes. The master node runs the control plane components, such as the API server, etc, and the kube-scheduler. The worker nodes run the container runtime and the kubelet, which communicates with the control plane to ensure that the desired state of the containers is maintained.

The cluster can be spread across multiple availability zones, regions, or even cloud providers to achieve high availability, scalability, and fault tolerance. Kubernetes also provides features such as auto-scaling, self-healing, and rolling updates, which allow it to automatically manage the resources available in the cluster and ensure that the applications running on it are highly available and performant.

Humalect platform creates and uses managed Kubernetes clusters like AWS EKS and Azure AKS provided by respective cloud providers.

## Getting started


The Clusters tab is present on the left sidebar, it helps you create new Clusters.

Use the `+ Create New Cluster` button in the top right corner to create or import new clusters.

We have set up 2 clusters below for reference.

![cluster-dashboard](./../../static/img/cluster-dashboard.png)




> You can also **import the cluster** by clicking on the drop-down menu of the `+ Create New Cluster`, situated at the right top.

## Cluster Viewing options
Humalect currently supports two types of Cluster Dashboard UI, they are:
**1. List view**
**2. Card view**

![cluster-view](./../../static/img/cluster-view.png)

You can also select the next drop-down option to select:
**1. Created Cluster**
**2. Imported Cluster**
**3. Deleted Cluster**


## Create New Cluster

To create a new cluster, click on the `+ Create New Cluster` button situated at the top right side.
Humalect provides the following Cloud Integration options for now:
**1. Amazon Web Services (AWS)**
**2. Microsoft Azure**

Feel free to request the cloud provider of your choice and we'll try to integrate it.


![create-cluster](./../../static/img/create-cluster.png)



Enter all the required details and hit `Create cluster` button. After you successfully create a cluster, you'll see a `Cluster creation in progress` bar, with a clickable button to see the Cluster creation `Logs`.

![cluster-creation](./../../static/img/cluster-creation.png)




## Created Clusters

Each created cluster has the following details associated with it. Refer to the chart below for more information on the same.


![created-cluster.png](./../../static/img/created-cluster.png)


Click on any of the clusters and you'll see a more detailed individual cluster view.


![cluster-details.png](./../../static/img/cluster-details.png)


Refer to the table below for various fields and values associated with created clusters.

> | Name | Desc |
> | --------------------- | ---- |
> | **Name** | Name of the cluster |
> | **Region** | cloud provider region in which cluster is created |
> | **cluster/cluster-delete** | Kubernetes version of cluster. |
> | **Public Subnets** | Network segment that allows external access to the cluster's resources and services via a public IP address. |
> | **Private Subnets** | Network segment that is not publicly accessible and is used for internal communication between cluster nodes.|
> | **DNS URL** | DNS URL for Load Balancer or CDN on which the domain is to be pointed |
> | **Instance Size / Nodes** | Type of machine instance used to create the cluster |
> | **VPC Name** | Virtual Private Cloud Name |
> | **Agent Version** | Version of humalect agent that is being used by cluster |
> | **Status** | Depicts whether the cluster is healthy or not. |
<center><i>Table showing Cluster details page values and their description. </i></center>



## Steps to Delete a Created Cluster
To delete a cluster,

**Step 1:** Go to the Clusters tab and identify the cluster which you wish to delete.
**Step 2:** From among the chosen cluster, click on the 3 dots that appear on the right side. A drop-down menu will open up with the following options as shown.

![cluster-delete.png](./../../static/img/cluster-delete.png)

**Step 3:** If the option to delete the cluster is not available to you, there can be 2 reasons for it.
- You are **not** the admin. Only users with admin access can delete clusters.
- Cluster deletion is not enabled in user settings, please enable it.

**Step 4:** Once you click on the `Delete` option, cluster deletion will start, you can click on `logs` from the UI to see the same as shown in the figure below.

![cluster-logs.png](./../../static/img/cluster-logs.png)


## Node Pools (disabled feature)

To create more Node Pools, click on the `Create New Pool`.

If you do not have any new pools created, it will show the default or existing pools e.g. `Pool(1 x Standard_A1_v2)`.

> **Note:** *You can also scale it up and down as per your desire.*



## Domains

Other than the domains that you provided during cluster creation, you can add more domains.

Select a cluster, Scroll down the cluster page, and you'll see a button `Add Domains`, click on it.


![add-domain-to-cluster](./../../static/img/add-domain-to-cluster.png)


You can add multiple domain names (make sure to link them with your DNS provider), then click on `Add to cluster` and you are good to go.


If your domain is not verified, you'll see the following error message.

![domain-not-verified](./../../static/img/domain-not-verified.png)


### Troubleshooting
Need help? [Contact](./../docs/Contact-us/reach-out-to-us) us

