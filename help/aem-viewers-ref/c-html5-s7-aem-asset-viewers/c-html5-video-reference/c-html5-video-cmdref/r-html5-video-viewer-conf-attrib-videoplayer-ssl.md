---
description: Konfigurationsattribut för Video Viewer.
solution: Experience Manager
title: VideoPlayer.ssl
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# VideoPlayer.ssl{#videoplayer-ssl}

Konfigurationsattribut för Video Viewer.

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

Se även [Säker videoleverans](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff).
