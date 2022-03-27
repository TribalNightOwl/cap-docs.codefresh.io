---
title: "What's new in CSDP?"
description: ""
group: whats-new
redirect_from:
  - /docs/whats-new/
toc: true
---

### 2022
We launched the Codefresh Software Delivery Platform (CSDP) in February this year. Built on Argo, the world’s most popular and fastest-growing open source software delivery, CSDP unlocks the full enterprise potential of Argo Workflows, Argo CD, Argo Events, and Argo Rollouts, providing a control-plane for managing them at scale.
Since the launch, we have continued to work on and grow CSDP, listening to what you had to say.

#### March 2022
This month's release focuses on key infrastructure enhancements in runtimes.

##### Kubernetes cluster server version
We now support the latest Kubernetes server versions, 1.22 and 1.23. 

##### Ingress controllers
We are continually working on supporting additional Ingress controllers, and this release includes support for four more of them:
* Ambassador
* NGINX Enterprise
* Istio
* Traefik

All ingress controllers must be configured to report their status. 
For details, see [Ingress controller requirements]({{site.baseurl}}/docs/runtime/requirements/#ingress-controller).


##### External cluster support
Argo CD can manage external clusters without Argo CD installed on them. CSDP offers the same functionality to add, view, and manage remote clusters.  
CSDP admins can add an external cluster to a CSDP runtime, and register it automatically as a managed cluster. From that point on, you have complete visibility into health and sync status, and options to manage them.  

With managed clusters in CSDP, you get:
* Streamlined management: All cluster- and cluster-component level operations are managed through the runtime, in a centralized location. You can install new and uninstall existing components, and remove the cluster from the runtime's managed list.
* Seamless upgrades: Upgrades to runtimes or to runtime components in the local cluster automatically upgrades those in managed clusters as well.
* Integration with CSDP dashboards: Applications dashboards reflect deployment information for applications in all managed clusters.

For details, see [Managed clusters]({{site.baseurl}}/docs/runtime/managed-clusters).

##### Topology views for runtime




