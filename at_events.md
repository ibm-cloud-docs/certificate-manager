---

copyright:
  years: 2018
lastupdated: "2018-06-22"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# {{site.data.keyword.cloudaccesstrailshort}} events  
{: #at_events}

Use the {{site.data.keyword.cloudaccesstrailfull}} service to track how users and applications interact with the {{site.data.keyword.cloudcerts_long}} service in the {{site.data.keyword.Bluemix}}. 
{:shortdesc}

The {{site.data.keyword.cloudaccesstrailfull_notm}} service records user-initiated activities that change the state of a service in the {{site.data.keyword.Bluemix_notm}}. For more information, see [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla). For example, when you import a certificate, an {{site.data.keyword.cloudaccesstrailshort}} event is generated.

The following table lists the API methods that generate an event when they are called:

<table>
  <caption>Actions that generate events</caption>
  <tr>
    <th>Action</th>
	  <th>Description</th>
  </tr>
  <tr>
    <td>cloudcerts.instance.create</td>
	  <td>Provision a {{site.data.keyword.cloudcerts_short}} instance.</td>
  </tr>
  <tr>
    <td>cloudcerts.instance.delete</td>
	  <td>Delete a {{site.data.keyword.cloudcerts_short}} instance.</td>
  </tr>
  <tr>
    <td>cloudcerts.certificate.import</td>
	  <td>Import a certificate that is issued by a third-party certificate authority.</td>
  </tr>
  <tr>
    <td>cloudcerts.certificate.read</td>
	  <td>Download a certificate.</td>
  </tr>
  <tr>
    <td>cloudcerts.certificates.list</td>
	  <td>List certificates.</td>
  </tr>
  <tr>
    <td>cloudcerts.certificates-metadata.list</td>
	  <td>List certificates metadata. Show details of a certificate.</td>
  </tr>
  <tr>
    <td>cloudcerts.certificates.search</td>
	  <td>Search certificates.</td>
  </tr>
  <tr>
    <td>cloudcerts.certificates-metadata.search</td>
	  <td>Search certificates metadata.</td>
  </tr>
  <tr>
    <td>cloudcerts.certificate.delete</td>
	  <td>Delete a certificate.</td>
  </tr>
  <tr>
    <td>cloudcerts.certificate.update</td>
	  <td>Update a certificate, for example, change the description of a certificate.</td>
  </tr>
</table>


 	
 


## Where to look for the events
{: #ui}

{{site.data.keyword.cloudaccesstrailshort}} events are available in the {{site.data.keyword.cloudaccesstrailshort}} **account domain** that is available in the {{site.data.keyword.Bluemix_notm}} region where the events are generated.

{{site.data.keyword.cloudaccesstrailshort}} events are automatically forwarded to the {{site.data.keyword.cloudaccesstrailshort}} service in the same region where the {{site.data.keyword.cloudcerts_short}} service is provisioned.


## Additional information
{: #info}

The field *requestData_str* includes the human readable name of the certificate.


