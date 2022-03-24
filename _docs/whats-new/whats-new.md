---
title: "What's new in CSDP?"
description: ""
group: whats-new
redirect_from:
  - /docs/whats-new/
toc: true
---

### 2022

#### March 2022
This month's release focuses on key infrastructure enhancements in runtimes.

##### Kubernetes cluster server version
We now support the latest Kubernetes server versions, 1.22 and 1.23. 

##### Ingress controllers
We are continually working on supporting additional Ingress controllers, and this release includes support for four more controllers:
* Ambassador
* NGINX Enterprise
* Istio
* Traefik

All ingress controllers must be configured to report their status. While Ambassador and Istio are configured by default to report their status, NGINX Enterprise and Traefik must be explicitly configured.  
For details, see [Ingress controller requirements]({{site.baseurl}}/docs/runtime/requirements/#ingress-controller).


##### External cluster support
Argo CD can manage external clusters without Argo CD installed on them. Now you can add, view, and manage remote clusters within CSDP.  
In CSDP, you simply add an external cluster to a CSDP runtime, and it is automatically registered as a managed cluster. From that point CSDP manages it as it manages the main cluster.  

With managed clusters in CSDP, you get:
* Streamlined management: All cluster- and cluster-component level operations are managed through the runtime, in a centralized location. You can install new and uninstall existing components, and remove the cluster from the runtime's managed list.
* Seamless upgrades: Upgrades to runtimes or to runtime components in the main cluster automatically upgrades those in managed clusters as well.
* Integration with CSDP dashboards: Applications dashboards reflect deployment information for applications in all managed clusters.

For details, see [Managed clusters]({{site.baseurl}}/docs/runtime/managed-clusters).

##### Topology views for runtime



### 2021

### November 2021

- Documentation site has been created and initiated. We invite all beta testers to provide their feedback through our dedicated [slack channel](https://codefresh.slack.com/archives/C02M5QBMXLN/p1637345778020900){:target="\_blank"} 
- A quick explanation of CAP entity model was added to our documentation - [documentation]({{site.baseurl}}/docs/configure-ci-cd-pipeline/triggers/git-triggers/#monorepo-support-modified-files)

### October 2021

- Codefresh Argo Platform beta program is finally launched. [Request Early Access](https://codefresh.io/codefresh-argo-platform/#sign-up){:target="\_blank"}
