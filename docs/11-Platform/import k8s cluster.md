---
title: Import an existing k8s cluster to Humalect
sidebar_position: 3
---

> ## This article covers:-
> 1. Import an existing Kubernetes Cluster to Humalect? <br/>
> 	a. For AWS <br/>
> 	b. For Azure



# Import an existing Kubernetes Cluster to Humalect

You can import an existing Kubernetes Cluster to Humalect. Follow along with the steps mentioned. 

## 1. For AWS
To import your existing Kubernetes cluster on AWS to Humalect, refer the following steps.

**Step 1:** Click on the `Import cluster` button present at the top right section as shown in the image.

![import-cluster](./../../static/img/import-cluster.png)
<center><i>Image showing Import cluster button. </i></center><br/>

**Step 2:** Select from the Cloud Integration drop-down menu your preferred cloud provider, `AWS / Azure`.


![import-cluster-2](./../../static/img/import-cluster-2.png)
<center><i>Image showing Import cluster page part 1. </i></center>


<br/>

![import-cluster-2](./../../static/img/import-cluster-3.png)
<center><i>Image showing Import cluster page part 2. </i></center>

<br/>

**Step 3:** Fill in the **Cluster name**. <br/>
**Step 4:** Specify **Domain(s)**. <br/>
**Step 5:** Choose **Cluster Region** from the following.  <br/>
`Mumbai /  Singapore / N. Virginia / Europe (Frankfurt) / Europe (Ireland) / Europe (London) / Europe (Paris) / Europe (Stockholm)
`<br/>
**Step 6:** Select a **VPC** from the drop down list (*the one that you already created*).<br/>
**Step 7:** Choose a **Monitoring Integrations**, `None / Datadog / Grafana`.<br/>
**Step 8:** Finally, click on the `Import Cluster` button to start importing your cluster. <br/>


---

## 2. For Azure
To import your existing Kubernetes cluster on Azure to Humalect, refer the following steps.

**Step 1:** Click on the `Import cluster` button present at the top right section as shown in the image.


![import-cluster](./../../static/img/import-cluster.png)
<center><i>Image showing Import cluster button. </i></center><br/>

**Step 2:** Select from the Cloud Integration drop-down menu your preferred cloud provider, `AWS / Azure`.


![import-cluster-azure](./../../static/img/import-cluster-azure.png)
<center><i>Image showing Import Cluster page. </i></center><br/>

**Step 3:** Fill in the **Cluster name**.<br/>
**Step 4:** Specify **Domain(s)**.<br/>
**Step 5:** Choose **Cluster Region** from the following. 
` East US / 
East US 2 / 
South Central US / 
West US 2 / 
West US 3 / 
Australia East / 
Southeast Asia / 
Central US /
Central India /  
East Asia /
Asia /
Asia Pacific / Jio India West / South India
`<br/>
**Step 6:** Finally, click on the `Import Cluster` button to start importing your cluster. 



### Troubleshooting
Need help? [Contact](https://docs.humalect.com/en/contact) us.