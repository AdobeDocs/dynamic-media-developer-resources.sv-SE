---
description: Konfigurationsattribut för visningsprogrammet för blandad media.
seo-description: Konfigurationsattribut för visningsprogrammet för blandad media.
seo-title: VideoPlayer.ssl
solution: Experience Manager
title: VideoPlayer.ssl
topic: Dynamic media
uuid: 07e2c55b-2388-44c8-83ab-338997c5cb71
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---


# VideoPlayer.ssl{#videoplayer-ssl}

Konfigurationsattribut för visningsprogrammet för blandad media.

>[!NOTE]
>
>Detta konfigurationsattribut gäller endast för AEM 6.2 med installation av [funktionspaket NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) och för AEM 6.1 med installation av [funktionspaket NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Kontrollerar om videon levereras via en säker SSL-anslutning (HTTPS) eller en osäker anslutning (HTTP). </p> <p>När värdet är <span class="codeph"> auto</span> ärvs videoleveransprotokollet från inbäddningswebbsidans protokoll. Om webbsidan läses in via HTTPS levereras videon också via HTTPS, och vice versa. Om webbsidan finns på HTTP, levereras videon via HTTP. </p> <p>Om <span class="codeph"> anges på</span> sker videoleveransen alltid via en säker anslutning utan hänsyn till webbsidans protokoll. </p> <p>Påverkar endast publicerad videoleverans och ignoreras för videoförhandsgranskning i redigeringsläge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

Se även [Säker videoleverans](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb).
