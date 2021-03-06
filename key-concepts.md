---

copyright:
  years: 2017, 2021
lastupdated: "2021-01-26"

keywords: certificates,ssl, tls, lifecycle, certificate, cert, devops process, domain ownership, certificate authority, free certificates, lets encrypt

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


# Key concepts
{: #key-concepts}

Learn about the concepts that are associated with certificates and how {{site.data.keyword.cloudcerts_full}} can help.
{: shortdesc}


## Certificate lifecycle
{: #life-cycle}

Check out the following image and descriptions to see how {{site.data.keyword.cloudcerts_short}} can help you manage the lifecycle of your certificates.

![How {{site.data.keyword.cloudcerts_short}} helps you to manage the certificate lifecycle.](images/cert-lifecycle.png){: caption="Figure 1. How {{site.data.keyword.cloudcerts_short}} helps you to manage the lifecycle of your certificates" caption-side="bottom"}


<dl>
  <dt>Order</dt>
    <dd>With {{site.data.keyword.cloudcerts_short}}, you can order free TLS (SSL) certificates through Let's Encrypt. If you already have a certificate authority that you prefer, you can bring your own certificate to the service.</dd>
  <dt>Store</dt>
    <dd>When you order a certificate through {{site.data.keyword.cloudcerts_short}}, it is automatically stored for you. If you bring your own certificate, you can easily import it into the service. You can also securely store the private key of a certificate alongside it.</dd>
  <dt>Deploy</dt>
    <dd>When you need to use your certificate, you can automate the deployment to TLS (SSL) termination points by integrating {{site.data.keyword.cloudcerts_short}} with DevOps processes. You can also use the <a href="/docs/containers?topic=containers-getting-started">IBM Cloud Kubernetes Service</a> CLI to easily deploy certificates from {{site.data.keyword.cloudcerts_short}}.</dd>
  <dt>Monitor and Alert</dt>
    <dd>The service continuously monitors your certificates for their expiration dates to notify you of upcoming expiring certificates and other lifecycle events such as reimports, orders, or renews through Slack or Callback URLs. If you have alerts that come from more than one service, it can be helpful to integrate with <a href="/docs/security-advisor?topic=security-advisor-getting-started">IBM Cloud Security Advisor</a> to manage all of your alerts in one place.</dd>
  <dt>Renew</dt>
    <dd>With {{site.data.keyword.cloudcerts_short}}, you can configure your certificates to be automatically renewed. When your certificate is renewed, the cycle begins again.</dd>
</dl>

## Examples
{: #life-cycle-examples}

* [How to Use {{site.data.keyword.cloudcerts_short}} to Avoid Outages Using Callback URLs - Part 1](https://www.ibm.com/cloud/blog/use-certificate-manager-avoid-outages-using-callback-urls){: external}

   Learn how to create GitHub issues for expiring certificate notifications.

* [How to Use {{site.data.keyword.cloudcerts_short}} to Avoid Outages Using Callback URLs - Part 2](https://www.ibm.com/cloud/blog/how-to-use-certificate-manager-to-avoid-outages-using-callback-urls-part-2){: external}

   Learn how to create PagerDuty incidents for expiring certificate notifications.

* [How to Automate TLS Certificate Rotation to Avoid Outages](https://www.ibm.com/cloud/blog/how-to-automate-tls-certificate-rotation-to-avoid-outages){: external}

   Learn how to automate certificate rotation for expiring certificates.  

* [How to validate a domain by using a Callback URL and a Cloud Function action)](https://www.ibm.com/cloud/blog/use-ibm-cloud-certificate-manager-to-obtain-lets-encrypt-tls-certificates-for-your-public-domains){: external}

   Learn how to validate your domain ownership when you order certificates.
