---
description: HTTPS-videoleverans
solution: Experience Manager
title: HTTPS-videoleverans
topic: Dynamic media
uuid: 7f8c1fe6-b464-4d80-9ffe-a36081825d49
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# HTTPS-videoleverans{#https-video-delivery}

>[!NOTE]
>
>Secure Video Delivery Gäller endast för AEM 6.2 med installationen av [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) och för AEM 6.1 med installationen av [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Förutsatt att visningsprogrammet fungerar i den konfiguration som beskrivs i början av det här avsnittet, kan publicerad videoleverans ske både i HTTPS-läge (säkert) och HTTP-läge (osäkert). I en standardkonfiguration följer leveransprotokollet strikt leveransprotokollet för inbäddningswebbsidan. Det går dock att tvinga fram HTTPS-video utan hänsyn till det protokoll som används när webbsidan bäddas in med konfigurationsattributet [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). (Observera att förhandsgranskning av video i redigeringsläge alltid levereras säkert via HTTPS.)

Beroende på vilken metod du använder för att publicera Dynamic Media-video i AEM används konfigurationsattributet `VideoPlayer.ssl` på ett annat sätt, vilket visas i följande exempel:

* Om du publicerar en Dynamic Media-video med en URL-adress lägger du till `VideoPlayer.ssl` i URL-adressen. Om du till exempel vill framtvinga en säker videoleverans lägger du till `&VideoPlayer.ssl=on` i slutet av följande exempel på visningsprogrammets URL:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   Se även [(Länka URL:er till ditt webbprogram](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Om du publicerar en Dynamic Media-video med inbäddad kod lägger du till `VideoPlayer.ssl` i listan över andra parametrar för visningsprogramkonfiguration i det inbäddade kodfragmentet. Om du till exempel vill tvinga HTTPS-videoleverans lägger du till `&VideoPlayer.ssl=on` som i följande exempel:

   ```
   <style type="text/css"> 
    #s7mixedmedia_div.s7mixedmediaviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/MixedMediaViewer.js"></script> 
   <div id="s7mixedmedia_div"></div> 
   <script type="text/javascript"> 
    var s7mixedmediaviewer = new s7viewers.MixedMediaViewer({ 
     "containerId" : "s7mixedmedia_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/MixedMedia_light", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "asset" : "/content/dam/Geometrixx-Outdoors-New-Launch/backpack/backpack_mixed_media" } 
    }).init(); 
   </script>
   ```

   Se även [(Bädda in videon på en webbsida](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

