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
We are continually extending support for more Ingress controllers, and this release adds support for these Ingress controllers:
* Ambassador
* NGINX Enterprise
* Istio
* Traefik

All ingress controllers must be configured to report their status. While Ambassador and Istio are configured by default to report their status, NGINX Enterprise and Traefik must be explicitly configured. For details, check out [Ingress controller requirements]({{site.baseurl}}/docs/runtime/requirements/#ingress-controller).


##### External cluster support
Add an external cluster to a CSDP runtime to register it as a managed cluster. External clusters do not have Argo CD installed on them but can be managed by the 
Managed clusters offer the 

* Simplified cluster management: A single Argo CD instance can manage multiple clusters in your organization. Unamanging a cluster is as simple as removing it from the runtime list.
* Robust security: Because not all users require access to managed clusters, it is easier to implement RBAC and other security features.
* Seamless upgrades: Upgrades to runtimes or to runtime components in the main cluster automatically upgrade managed clusters as well.
* Integration with CSDP dashboards: Applications dashboards reflect deployment information from all managed clusters.

For details, see [Managed clusters]({{site.baseurl}}/docs/runtime/managed-clusters).

##### Topology views for runtime



### 2021

### November 2021

- Documentation site has been created and initiated. We invite all beta testers to provide their feedback through our dedicated [slack channel](https://codefresh.slack.com/archives/C02M5QBMXLN/p1637345778020900){:target="\_blank"} 
- A quick explanation of CAP entity model was added to our documentation - [documentation]({{site.baseurl}}/docs/configure-ci-cd-pipeline/triggers/git-triggers/#monorepo-support-modified-files)

### October 2021

- Codefresh Argo Platform beta program is finally launched. [Request Early Access](https://codefresh.io/codefresh-argo-platform/#sign-up){:target="\_blank"}
