---

copyright:
  years: 2017, 2021
lastupdated: "2021-06-25"

keywords: Certificate Manager, endpoints, service endpoints, regions, available regions

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



# Regions and endpoints
{: #regions-endpoints}

Review region and connectivity options for interacting with {{site.data.keyword.cloudcerts_long}}.

## Available regions
{: #regions}

You can create {{site.data.keyword.cloudcerts_short}} resources in one of the supported {{site.data.keyword.cloud_notm}} regions, which represent the geographic areas where your {{site.data.keyword.cloudcerts_short}} requests are handled and processed.

- Dallas (`us-south`)
- Frankfurt (`eu-de`)
- London (`eu-gb`)
- Osaka (`jp-osa`)
- Sydney (`au-syd`)
- Tokyo (`jp-tok`)
- Toronto (`ca-tor`)
- Washington DC (`us-east`)



## Connectivity options
{: #connectivity}

{{site.data.keyword.cloudcerts_short}} offers two connectivity options for interacting with its service APIs.

<dl>
  <dt>Public endpoints</dt>
    <dd>By default, you can connect to resources in your account over the {{site.data.keyword.cloud_notm}} public network. Your data is encrypted in transit by using the Transport Security Layer (TLS) 1.2 protocol.
    </dd>
  <dt>Private endpoints</dt>
    <dd>For added benefits, you can also enable [virtual routing and forwarding (VRF) and service endpoints](/docs/account?topic=account-vrf-service-endpoint) for your {{site.data.keyword.cloud_notm}} account. When you enable VRF for your account, you can [connect to {{site.data.keyword.cloudcerts_short}} by using a private IP](/docs/certificate-manager?topic=certificate-manager-service-connection) that is accessible only through the {{site.data.keyword.cloud_notm}} private network.
    </dd>
</dl>

## Service endpoints
{: #endpoints}

If you are managing your certificates programmatically, see the following table to determine the API endpoints to use when you connect to the {{site.data.keyword.cloudcerts_short}} API.

| Region        | Endpoint                                     |
| ------------- | -------------------------------------------- |
| Dallas        | `us-south.certificate-manager.cloud.ibm.com` |
| Frankfurt     | `eu-de.certificate-manager.cloud.ibm.com`    |
| London        | `eu-gb.certificate-manager.cloud.ibm.com`    |
| Osaka         | `jp-osa.certificate-manager.cloud.ibm.com`   |
| Sydney        | `au-syd.certificate-manager.cloud.ibm.com`   |
| Tokyo         | `jp-tok.certificate-manager.cloud.ibm.com`   |
| Toronto       | `ca-tor.certificate-manager.cloud.ibm.com`   |
| Washington DC | `us-east.certificate-manager.cloud.ibm.com`  |
{: caption="Table 1. Lists public endpoints for interacting with {{site.data.keyword.cloudcerts_short}} APIs over {{site.data.keyword.cloud_notm}}'s public network" caption-side="top"}
{: #private-endpoints}
{: tab-title="Public"}
{: tab-group="service-endpoints"}
{: class="simple-tab-table"}

| Region        | Endpoint                                             |
| ------------- | ---------------------------------------------------- |
| Dallas        | `private.us-south.certificate-manager.cloud.ibm.com` |
| Frankfurt     | `private.eu-de.certificate-manager.cloud.ibm.com`    |
| London        | `private.eu-gb.certificate-manager.cloud.ibm.com`    |
| Osaka         | `private.jp-osa.certificate-manager.cloud.ibm.com`   |
| Sydney        | `private.au-syd.certificate-manager.cloud.ibm.com`   |
| Tokyo         | `private.jp-tok.certificate-manager.cloud.ibm.com`   |
| Toronto       | `ca-tor.certificate-manager.cloud.ibm.com`           |
| Washington DC | `private.us-east.certificate-manager.cloud.ibm.com`  |
{: caption="Table 1. Lists private endpoints for interacting with {{site.data.keyword.cloudcerts_short}} APIs over {{site.data.keyword.cloud_notm}}'s private network" caption-side="top"}
{: #public-endpoints}
{: tab-title="Private"}
{: tab-group="service-endpoints"}
{: class="simple-tab-table"}

### Notes
{: #endpoints-notes}

- In the Frankfurt region only, your certificates are maintained in the service database over the public network.
- If you need to manage resources on {{site.data.keyword.cloud_notm}}'s private network, using {{site.data.keyword.openwhisk}} as Callback URL servers is not recommended. {{site.data.keyword.openwhisk_short}} does not yet support private endpoints. To learn more, check out the [{{site.data.keyword.openwhisk_short}} docs](/docs/openwhisk?topic=openwhisk-getting-started).
- Let's Encrypt is a third-party service that runs outside of {{site.data.keyword.cloud_notm}}. When you order certificates through Let’s Encrypt, {{site.data.keyword.cloudcerts_short}} interacts with Let's Encrypt over the public network.