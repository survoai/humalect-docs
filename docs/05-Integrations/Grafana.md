---
sidebar_position: 6
title: 5. Grafana Cloud
---

> ## This article covers
> 1. What is Grafana?
> 2. Prerequisites
> 3. Connect Grafana with Humalect

**Humalect** provides Grafana as one of the open source Monitoring integrations.

Grafana Cloud is a cloud-based version of Grafana, an open-source platform for monitoring and analytics. It allows users to easily create and share dashboards, alerts, and other visualizations of their data. 

It provides a scalable and reliable infrastructure for running Grafana, so users don't have to worry about managing and maintaining the software themselves.

## Prerequisites
1. You need to have a cloud account (AWS / Azure) connected with Humalect.


## Connect Grafana with Humalect

Under the `Connect Your Monitoring Tool` section, select `Grafana` and follow the mentioned steps. 

**Step 1**. Click on the `Connect` button present in the UI.

![grafana-connect](./../../static/img/grafana-connect.png)

**Step 2.** Fill in the following details and hit `Connect`:-


![grafana-enter-deets](./../../static/img/grafana-enter-deets.jpeg)

|Sl. | Field-1| Field-2 | Field-3 (generated token) | 
| -- | -- | -- | --- |
|1. | Grafana URL | - | - |
|2. | Prometheus URL |  Prometheus Username| Prometheus Password |
|3. | Loki URL  | Loki Username| Loki Password |


After you have successfully entered the above details, you'll see a screen shown in the image below welcoming you to Grafana Cloud. 

![grafana-welcom](./../../static/img/grafana-welcom.jpeg)

### Where to get these details from?


:::info
Find all the details mentioned below from here - https://grafana.com/orgs/priyansh1/
P.s. - Change the username to your organization name. 
:::


![grafana-all](./../../static/img/grafana-all.jpeg)

Click on `Details` button of the stack you wish to know the credentials for.

![grafana-url-deets](./../../static/img/grafana-url-deets.jpeg)
<center><i> Image showing Grafana Details. </i></center> <br/>


![loki-deets](./../../static/img/loki-deets.jpeg)
<center><i> Image showing Loki Details. </i></center> <br/>


![prometheus-deets](./../../static/img/prometheus-deets.jpeg)
<center><i> Image showing Prometheus Details. </i></center> <br/>






**Step 3.** You'll see `✅ Successful` checkmark and you successfully connected Grafana. 

![grafana-success](./../../static/img/grafana-success.png)

**Step 4.** Once Grafana is connected, click on the external link icon to take it to your connected Grafana dashboard. 

![grafana-dashboard](./../../static/img/grafana-dashboard.jpeg)

The above picture shows various metrics dashboards of the apps connected to Humalect platform. 



### Troubleshooting
Need help? Contact [Humalect support.](https://humalect.com/)