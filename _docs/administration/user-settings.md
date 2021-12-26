---
title: "User settings"
description: ""
group: administration
toc: true
---

User settings lets you define policies for Codefresh build notifications, support login with your user alias, and API keys to access Codefresh functionality.

### Access user settings

Go to [User Settings](https://g.codefresh.io/2.0/user-settings){:target="\_blank"}. 

{% include
image.html
lightbox="true"
file="/images/administration/user-settings/main.png"
url="/images/administration/user-settings/main.png"
alt="User settings"
caption="User settings"
max-width="70%"
%}

### Select email notifications for builds 

Decide which notifications to activate for Codefresh builds. By default, when your account is set up, notifications are turned on for both successful and failed builds.

* The email address is by default, populated with the same address you used to [sign-up]({{site.baseurl}}/docs/getting-started/create-a-codefresh-account/). 
If needed, enter a different email address for build notifications.
* Turn on notifications:
  * Only for successful builds
  * Only for failed builds
  * Only when your email is the Git committer. This option is especially useful in big team where multiple users commit to the same Git repository.

{% include image.html
lightbox="true"
file="/images/administration/user-settings/email-notifications.png"
url="/images/administration/user-settings/email-notifications.png"
alt="Email notifications"
caption="Email notifications"
max-width="50%"
%}


### Get weekly updates on build usage

When selected, build usage updates sends a weekly summary of your builds across your pipelines along with other statistics. This information is useful to understand your overall project build health and capacity usage.


### Enable access for support personnel

Enabling Codefresh support access to your system is useful to troubleshoot issues you may experience issues with the Codefresh platform.
When selected our support personnel can log into your account, look at running builds, inspect your docker images, run pipelines, and perform other actions as required. Otherwise, our support staff have **zero visibility** to your account. 

> Important: Codefresh audits all actions performed by Codefresh support on your account. Codefresh *always coordinate with you* prior to taking any action that can impact your system, such as running a pipeline.

{% include image.html
lightbox="true"
file="/images/administration/user-settings/user-support-access.png"
url="/images/administration/user-settings/user-support-access.png"
alt="Allow access to support"
caption="Allow access to support"
max-width="50%"
%}


### Generate API keys

API keys allow access to Codefresh functionality outside the UI, from scripts or applications, as from the Codefresh command line for example. Generate one or more API keys, and select the scopes for each API key. Once you generate an API key, you can edit the scopes associated with it, and revoke the key.

>Tokens are visible only during creation. You cannot "view" an existing token. If you want to re-enable API access for an existing application, you need to delete the old token and create a new one.


  {% include image.html
lightbox="true"
file="/images/integrations/api/generate-token.png"
url="/images/integrations/api/generate-token.png"
alt="Generate API keys"
caption="Generate API key"
max-width="50%"
%}

  {% include image.html
lightbox="true"
file="/images/integrations/api/user-api-scope.png"
url="/images/integrations/api/user-api-scope.png"
alt="Select API key scopes"
caption="Select API key scopes"
max-width="50%"
%}


### What to read next
[Add users]({{site.baseurl}}/docs/administration/add-users/)  
[Single Sign on]({{site.baseurl}}/docs/administration/single-sign-on/)
