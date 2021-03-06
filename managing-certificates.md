---

copyright:
  years: 2017, 2021
lastupdated: "2021-06-02"

keywords: certificates, ssl, tls, manage certificates, cert ui, third-party issuer, pem format, openssl, import certificate, download certificate, renew certificates

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


# Managing certificates from the dashboard
{: #managing-certificates-from-the-dashboard}

You can use the {{site.data.keyword.cloudcerts_full}} service dashboard to manage certificates that you obtain from third-party issuers, or order from {{site.data.keyword.cloudcerts_short}}, to use with your {{site.data.keyword.IBM_notm}} cloud-based apps or services.
{: shortdesc}

## Supported certificate formats and public key algorithms
{: supported-formats-and-algorithms}

### Certificate formats
* PEM

Review the OpenSSL documentation to learn how to convert other certificate formats, such as P12 and CRT, to PEM.
{: note} 

### Public key algorithms
* Rivest-Shamir-Adleman (RSA)
* Digital Signature Algorithm (DSA)
* Elliptic Curve Digital Signature Algorithm (ECDSA)
* Elliptic Curve with Diffie-Hellman key agreement protocol (ECDH)

## Importing a certificate
{: #importing-a-certificate}

To start managing your certificates, import them into {{site.data.keyword.cloudcerts_short}}.
{: shortdesc}

### Before you begin
{: #importing-before}

* Create a valid, unexpired certificate with a matching private key (key is optional).
* Convert the files into Privacy-enhanced Electronic Mail (PEM) format.
* The certificate must be an X.509 compliant certificate.
* Keep the private key unencrypted to ensure that it can be imported.

To import a certificate, click **Import Certificate** and provide the following details:

1. Provide a certificate name.
2. Select the certificate file in PEM format by clicking **Browse**.
3. Optional: Select the certificate's private key in PEM format by clicking **Browse**.
4. If applicable, provide the intermediate certificate file in PEM format.
5. Optional: Enter a description.
6. Click **Import**.

After you import a certificate, the following information is displayed in the Certificates table. To view more information about the certificate, you can click on the certificate row in the Certificates table.

| Component | Description | 
|-----|----| 
| Name | A meaningful display name. The maximum length is 256 characters. |
| Description | (Optional) Descriptive text for the certificate. The maximum length is 1024 characters. |
| Domain | The domain or domains for which the certificate is valid. |
| Issuer | The certificate authority (CA) that issued the certificate. |
| Algorithm | The certificate signature algorithm. |
| Key algorithm | The public key algorithm |
| Expires in | The number of remaining days before the certificate is no longer valid. |
| Valid from | The date on which the certificate became valid, in Coordinated Universal Time time zone. |
| Expires on | The date on which the certificate is no longer valid (in Coordinated Universal Time time zone). |
| Status | The status of your certificate. |
| Certificate ID | The generated ID given to the certificate upon import. |
{: caption="Table 1. Information about the imported certificate" caption-side="top"}

</br>

## Reimporting a certificate
{: #reimport-certificate}

If your certificate is about to expire, you can update it by importing a new version that has the same domain as the existing certificate, but has a new expiry date. When a certificate is reimported, the existing version of the certificate is retained as a backup that can be downloaded if required.
{: shortdesc}

### Reimporting your certificate
{: #reimporting-certificate}

To reimport a certificate, complete the following steps:

1. Click on the side menu for the requested certificate.
2. Click **Reimport Certificate**.
3. Select the new certificate file in PEM format by clicking **Browse**.
4. (Optional) Select the new certificate's private key in PEM format by clicking **Browse**.
5. (Optional) Provide a new intermediate certificate file in PEM format by clicking **Browse**.
6. Click **Reimport** and then **Done**.

You can attempt to reimport a certificate up to five times per minute.
{: note}

### Downloading a previous version of your certificate
{: #downloading-certificate}

To download the previous version of a certificate, complete the following steps:

1. Click on the row side menu for the requested certificate.
2. Click the **Previous version** button.

## Ordering certificates
{: #order-certificates}

Before you order a certificate, [first complete the required setup](/docs/certificate-manager?topic=certificate-manager-ordering-certificates).  
To order a certificate, click **Order Certificate**, select either **{{site.data.keyword.cis_full_notm}}** or **Another DNS Provider** and provide the following details:

1. Certificate name.
2. Certificate authority.
3. Required domains.
4. Appropriate algorithm and key algorithm.
5. Click **Order**.

Ordering certificates is limited to five orders/minute per {{site.data.keyword.cloudcerts_short}} instance, 100 orders per hour per IBM user account, and five certificates for the same domains per week.
{: note}

## Renewing certificates
{: #renew-certificates}

You can manually or automatically renew certificates that you order through {{site.data.keyword.cloudcerts_short}}. You can also disable the auto-renewal feature after you enable it.

Renewing a certificate has the following limitations: 

* Five renewal requests per certificate, per minute.
* One 100 renewal requests per hour, within each IBM user account.

### Automatically renewing certificates
{: #renew-auto}

You can set a certificate to automatically renew while you're ordering. Or, you can enable auto-renewal after it's configured. 

* To enable auto-renewal while ordering a certificate, toggle **Auto-renewal** to **On**.
* To enable auto-renewal for a certificate that you already own, select **Enable auto-renewal** from a certificates side menu.

### Manually renewing certificates
{: #renew-manual}

If you need to manually renew your certificates, complete the following steps.

1. Click the menu in the row of the certificate you want to renew.
2. Click **Renew Certificate**.
3. Optional: You can choose to rekey your certificate by checking the **Rekey certificate** checkbox. This renews your certificate with a new key pair.

  When you rekey a certificate, make sure to deploy the new certificates and keys everywhere they are in use.
  {: note}
  
4. Click **Renew**.


### Stopping automatic renewal
{: #renew-stop}

To disable automatic renewal, select **Disable auto-renewal** from the certificates menu.


## Searching certificates
{: #searching-certificates}

If you manage many certificates, you can use the search bar to locate the required certificate.
{: shortdesc}

* To search for a certificate name, domain, or issuer, start to type your term into the search bar and press **Enter**.
* To search for an exact value, enclose your search term with double quotation marks.
* To view all of your certificates, click the **X** icon in the search bar.

## Downloading certificates
{: #downloading-certificates}

When you are ready to deploy your certificate to your app or service, you can download the certificate and the associated private key.
{: shortdesc}

To download a certificate, complete the following steps:

1. Select the checkbox for the certificate that you want to download.
2. Click **Download Certificate**. Depending on what you imported into the service, you receive a compressed file that contains PEM files for the certificate, an associated private key, and an associated intermediate certificate.

You cannot download expired certificates.
{: note}

## Deleting certificates
{: #deleting-certificates}

If you want to stop tracking a certificate, you can delete it.
{: shortdesc}  

To delete a certificate, complete the following steps:

1. Select the checkbox for the certificate that you want to delete.
2. Click the **Trash** icon.

## Updating certificate metadata
{: #updating-certificates-metadata}

You can also update the name and description of a certificate.
{: shortdesc}

To update a certificate, complete the following steps:

1. Select a row to open the details for that certificate.
2. Update the name or description.
3. Save your changes.

You can perform up to five update actions per minute.
{: note}
