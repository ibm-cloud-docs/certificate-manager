---

copyright:
  years: 2018
lastupdated: "2018-11-15"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}

# Note sulla release
{: #release-notes}

Sono disponibili le seguenti funzioni e modifiche al servizio {{site.data.keyword.cloudcerts_long}}.

## 14 novembre 2018
{: 14November2018}

- **Reimportazione**  
  Puoi aggiornare un certificato reimportando una nuova versione che ha lo stesso dominio del certificato esistente ma che ha una nuova data di scadenza. Quando un certificato viene reimportato, la versione esistente del certificato viene conservata come un backup; vedi [Reimportazione di un certificato](/docs/services/certificate-manager/managing-certificates.html#reimport-certificate).

- **1000 certificati per istanza**  
  Puoi importare fino a 1000 certificati per istanza.

## 28 ottobre 2018
{: 28October2018}

- **Banner di annunci**  
  Gli annunci di servizio, quali le indicazioni di obsolescenza delle API e altre notizie, vengono visualizzati nella scheda **Gestisci**.

## 12 settembre 2018
{: 12September2018}

- **Il nome del certificato è obbligatorio**  
  È obbligatorio fornire un valore per il nome del certificato quando lo importi.  

- **API obsolete**  
  Le API **Import a certificate** e **Update a certificate's metadata** v2 sono state dichiarate obsolete e verranno rimosse il 1° dicembre 2018. Devi eseguire un upgrade alle API v3. Per ulteriori informazioni, [vedi la documentazione API ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/apidocs/certificate-manager).

- **Notifiche Slack raggruppate**  
  Le notifiche in Slack sono raggruppare per data di scadenza.

## 2 settembre 2018
{: 2September2018}

- **{{site.data.keyword.cloudcerts_long_notm}} è generalmente disponibile**  
  Il servizio {{site.data.keyword.cloudcerts_short}} è generalmente disponibile (GA) in {{site.data.keyword.cloud_notm}}.

## 22 agosto 2018
{: 22August2018}

- **Live a Londra**  
  {{site.data.keyword.cloudcerts_long_notm}} Beta è disponibile nella località di Londra.

## 15 agosto 2018
{: 15August2018}

- **Rimosse le API v1 obsolete**  
  Le API versione 1 non sono più disponibili. Se non hai ancora aggiornato la tua API, devi farlo il prima possibile. Per ulteriori informazioni, [vedi la documentazione API ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/apidocs/).

- **I ruoli della piattaforma sono stati sostituiti con i ruoli del servizio**  
  Puoi controllare l'accesso alle istanze di {{site.data.keyword.cloudcerts_short}} utilizzando i ruoli del servizio. [Ulteriori informazioni sulla gestione dell'accesso](access-management.html).

## 12 luglio 2018
{: 12July2018}

- **Callback delle notifiche**  
  È stato aggiunto il supporto di callback alle notifiche. Puoi scegliere se inviare le notifiche allo slack o di utilizzare un qualsiasi URL di callback per inviare le notifiche. Ad esempio, puoi inviare notifiche a PagerDuty, aprire automaticamente un problema in GitHub o attivare gli script di rinnovo. [Ulteriori informazioni sulle notifiche](notifications-dashboard.html).

## 12 giugno 2018
{: 12June2018}

- **Notifiche slack**  
  Sono state aggiunte le notifiche Slack in modo che non ti perderai mai un certificato in scadenza. [Ulteriori informazioni sulle notifiche](notifications-dashboard.html).

## 8 gennaio 2018
{: 8January2018}

- **API obsolete**  
  Le API Versione 1 sono obsolete e saranno rimosse l'8 settembre 2018. Devi eseguire un upgrade alle API v2. Per ulteriori informazioni, [vedi la documentazione API ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/apidocs/certificate-manager).

## 19 dicembre 2017
{: 19December2017}

- **{{site.data.keyword.cloudcerts_long_notm}} è disponibile come un servizio beta**  
  Il servizio {{site.data.keyword.cloudcerts_short}} è disponibile come un servizio beta in {{site.data.keyword.cloud_notm}}.