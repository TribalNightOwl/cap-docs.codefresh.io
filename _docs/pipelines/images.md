---
title: "Viewing Images in CSDP"
description: ""
group: pipelines
toc: true
---

Building Docker images is one of the most basic requirements for creating Delivery Pipelines. 
Once you create an image, push the image to a registry, and report it to CSDP, image information is continually updated in the CSDP UI. 

### Requirements for images in CSDP
Complete the mandatory steps to see your images in CSDP. Each step has links to examples in the Codefresh Hub for Argo.  

1. (Mandatory) Build the Docker image, and push the image to any registry.  
  See [Create a Docker image using Kaniko](https://codefresh.io/argohub/workflow-template/kaniko){:target="\_blank"}.
1. (Optional) Enrich image information with annotations and metadata.  
  For Git and Jira image enrichment examples, see [CSDP-metadata image enrichment](https://codefresh.io/argohub/workflow-template/CSDP-metadata){:target="\_blank"}.
1. (Mandatory) Report image information to CSDP.  
  See the [report-image-info](https://github.com/codefresh-io/argo-hub/blob/main/workflows/codefresh-csdp/versions/0.0.6/docs/report-image-info.md){:target="\_blank"} example.
  

### Image views in CSDP 
* In the CSDP UI, go to [Images](https://g.codefresh.io/2.0/images){:target="\_blank"}.

Image views are layered to show three levels of data: 
* Repository and application deployment
* Tags
* Summary with metadata and binary information 

#### Filters for image views
As with any resource in CSDP, image views support filters that allow you focus on the data that's important to you.
Most image filters support multi-selection.  Unless otherwise indicated, the filters are common to all view levels.

{: .table .table-bordered .table-hover}
|  Filter          |  Description|  
| --------------   | --------------           |  
| **Repository Names** | The Git repository or repositories that contain the image.  |                            
| **Tag**              | The tag by which to filter. |  
| **Registry Types**   | The registry which stores your image. To filter by registries that are not listed, select **Other types**.|
| **Git branch**       | The Git branch to which the image is pushed.|
| **Git repositories** | The Git provider you use.|      
| **Deployed in application**| The application or applications in which the image is currently deployed.|
| **Sorted by** | List images by **Name**, or by the most recent update, **Last update**.



#### Image repository and deployment view
The default view for image resources shows repository and deployment information.

{% include 
   image.html 
   lightbox="true" 
   file="/images/image/application-level.png" 
   url="/images/image/application-level.png" 
   alt="Repository & deployment info for Images in CSDP" 
   caption="Repository & deployment info for Images in CSDP"
   max-width="30%" 
   %}

{: .table .table-bordered .table-hover}
|  Legend          |  Description|  
| --------------   | --------------           |  
| **1**            | The name of the image.   |                            
| **2**            | The applications in which the image is currently deployed. Select the application to go to the Applications dashboard.|  
| **3**            | The details on the most recent commit associated with the image. Select the commit to view the changes in the Git repository.|
| **4**            | Binary information on the image.|
| **5**            | The registry to which the image is pushed, and from which it is distributed.|
                     
### Image tag view
Drilldown on the repository shows tag information for the image.
{% include 
   image.html 
   lightbox="true" 
   file="/images/image/tag-view.png" 
   url="/images/image/tag-view.png" 
   alt="Tag info for Images in CSDP" 
   caption="Tag info for Images in CSDP"
   max-width="30%" 
   %}

{: .table .table-bordered .table-hover}
|  Legend          |  Description|  
| --------------   | --------------           |  
| **1**                | The image tag.   |                            
| **2**                | The comment describing the commit or change, with the name of the Git provider and the corresponding PR. To view details of the commit changes in the Git repository, select the commit text.|  
| **3**                | The hash of the Docker image, generated as sha256. A change in the digest indicates that something has changed in the image.|
| **4**                | The registry to which the image is pushed (stored), and from which it is distributed.|
| **5**                | The OS and architecture in which the image was created. The date and time of the most recent update is in the local time zone|       
| **6**                | Additional information on the image. To view the Summary, select **more details**.|

###  Image summary view
The Summary view shows metadata for the image. 
Selecting **more details** for an image tag.

{% include 
   image.html 
   lightbox="true" 
   file="/images/image/summary-view.png" 
   url="/images/image/summary-view.png" 
   alt="Summary info for Images in CSDP" 
   caption="Summary info for Images in CSDP"
   max-width="30%" 
   %}

{: .table .table-bordered .table-hover}
|  Legend          |  Description|  
| --------------   | --------------           |  
| **1**            | The bugs or fix requests opened and being worked on for this image tag. |                            
| **2**            | The pull request or requests pending commit.|  
| **3**            | The Git details for this image tag, such as the Git hash, the Jira issue number, Git Pull Request, commit information, the name of the user who performed the commit. |       
| **4**            | The workflow for the image step. Select to go to the Workflow.| 
| **5**             | The log information for the build image step in the relevant workflow. Select to view Logs panel. |
