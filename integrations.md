---

copyright:
  years: 2017, 2021
lastupdated: "2021-06-02"

keywords: certificates, ssl, tls, integrations, kube, kubernetes, custom domain

subcollection: certificate-manager

---

{:codeblock: .codeblock}
{:screen: .screen}
{:download: .download}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}
{:gif: data-image-type='gif'}
{:important: .important}
{:note: .note}
{:pre: .pre}
{:tip: .tip}
{:preview: .preview}
{:deprecated: .deprecated}
{:beta: .beta}
{:term: .term}
{:shortdesc: .shortdesc}
{:script: data-hd-video='script'}
{:support: data-reuse='support'}
{:table: .aria-labeledby="caption"}
{:troubleshoot: data-hd-content-type='troubleshoot'}
{:help: data-hd-content-type='help'}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:tsSymptoms: .tsSymptoms}
{:java: .ph data-hd-programlang='java'}
{:javascript: .ph data-hd-programlang='javascript'}
{:swift: .ph data-hd-programlang='swift'}
{:curl: .ph data-hd-programlang='curl'}
{:video: .video}
{:step: data-tutorial-type='step'}
{:tutorial: data-hd-content-type='tutorial'}


# Available integrations
{: #available-integrations}

The following tables lists supported integrations by {{site.data.keyword.cloudcerts_full}}.

## Services that are integrated with {{site.data.keyword.cloudcerts_short}}
{: #service-integrations-1}

| Service | Description | 
|-----|----| 
| {{site.data.keyword.containerlong_notm}} and {{site.data.keyword.openshiftlong_notm}} | By default, a {{site.data.keyword.cloudcerts_short}} instance in the format `kube-<cluster_ID>` is automatically created for each cluster that you can use to store and manage the cluster's TLS certificates. Cluster administrators can use the [{{site.data.keyword.containerlong_notm}} plug-in commands](/docs/containers?topic=containers-cli-plugin-kubernetes-service-cli#cs_ingress_secret_create) to import TLS certificates as Kubernetes secrets and to update secrets with a new certificate without causing downtime. To get started, check out the [Ingress TLS documentation](/docs/containers?topic=containers-ingress-types#manage_certs). Do not delete your cluster's default {{site.data.keyword.cloudcerts_short}} instance. |
| {{site.data.keyword.cloud_notm}} {{site.data.keyword.apigw_short}} | Store your custom domain certificates in the {{site.data.keyword.cloudcerts_short}} service, then use certificate CRNs to bind with custom domains in {{site.data.keyword.apigw_short}}. [Learn more about custom endpoints in {{site.data.keyword.apigw_short}}](/docs/api-gateway?topic=api-gateway-custom_endpoint). |
| IBM Cloud Load Balancer for VPC | A TLS certificate is required for load balancers to perform TLS offloading tasks. You may manage the TLS certificates through {{site.data.keyword.cloudcerts_short}}. Enable service-to-service authorization to give a load balancer access to your certificate. [Learn more about this integration](/docs/vpc?topic=vpc-load-balancers#ssl-offloading-and-required-authorizations) |
{: caption="Table 1. {{site.data.keyword.cloud_notm}} services that provide an integration with {{site.data.keyword.cloudcerts_short}}" caption-side="top"}

## Services that {{site.data.keyword.cloudcerts_short}} is integrated with
{: #service-integrations-2}

| Service | Description | 
|-----|----| 
| {{site.data.keyword.cis_full_notm}} | Order Let's Encrypt certificates with ease by leveraging {{site.data.keyword.cis_full_notm}} as your DNS provider. To get started, see the [Ordering certificates](/docs/certificate-manager?topic=certificate-manager-ordering-certificates) documentation. |
| IBM Cloud Identity and Access Management | Access to the service and the resources that it contains are managed by using [Identity and Access Management](/docs/account?topic=account-iamoverview). | 
| Security Insights | [Security Insights](/docs/security-advisor?topic=security-advisor-getting-started#getting-started) (formerly known as {{site.data.keyword.security-advisor_short}}) centralizes the information about {{site.data.keyword.cloud_notm}} services. The information includes the indication of expired certificates and certificates that are about to expire in instances of {{site.data.keyword.cloudcerts_short}} in your {{site.data.keyword.cloud_notm}} account. [Learn more about Security Insights](/docs/security-advisor?topic=security-advisor-getting-started#getting-started). |
| {{site.data.keyword.at_full_notm}} | You can use [{{site.data.keyword.at_short}}](/docs/activity-tracker?topic=activity-tracker-getting-started) to track how users and applications interact with the {{site.data.keyword.cloudcerts_long_notm}} service in the {{site.data.keyword.cloud_notm}}. To get the list of actions that generate an event, see [Auditing events for {{site.data.keyword.cloudcerts_short}}](/docs/certificate-manager?topic=certificate-manager-at_events#at_events). |
| {{site.data.keyword.la_full_notm}} | You can use [{{site.data.keyword.la_short}}](/docs/log-analysis?topic=log-analysis-getting-started) offers administrators, DevOps teams, and developers advanced features to filter, search, and tail log data, define alerts, and design custom views to monitor application and system logs related to {{site.data.keyword.cloudcerts_short}}. To get started, see [Viewing logs for {{site.data.keyword.cloudcerts_short}}](/docs/certificate-manager?topic=certificate-manager-log_events#log_events). |
{: caption="Table 2. {{site.data.keyword.cloud_notm}} services that {{site.data.keyword.cloudcerts_short}} provides an integration for." caption-side="top"}
