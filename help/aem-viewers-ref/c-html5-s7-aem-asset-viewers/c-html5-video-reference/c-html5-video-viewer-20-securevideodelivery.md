---
description: 'null'
seo-description: 'null'
seo-title: HTTP-videoleverans
solution: Experience Manager
title: HTTP-videoleverans
topic: Dynamic media
uuid: fd02a55a-a0f1-47a2-983f-15f296d1dbb4
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# HTTP-videoleverans{#http-video-delivery}

>[!NOTE]
>
>Secure Video Delivery Gäller endast för AEM 6.2 med installationen av [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) och för AEM 6.1 med installationen av [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Förutsatt att visningsprogrammet fungerar i den konfiguration som beskrivs i början av det här avsnittet, kan publicerad videoleverans ske både i HTTPS-läge (säkert) och HTTP-läge (osäkert). I en standardkonfiguration följer leveransprotokollet strikt leveransprotokollet för inbäddningswebbsidan. Det går dock att tvinga fram HTTPS-video utan hänsyn till det protokoll som används när webbsidan bäddas in med konfigurationsattributet [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). (Observera att förhandsgranskning av video i redigeringsläge alltid levereras säkert via HTTPS.)

Beroende på vilken metod du använder för att publicera Dynamic Media-video i AEM används konfigurationsattributet `VideoPlayer.ssl` på ett annat sätt, vilket visas i följande exempel:

* Om du publicerar en Dynamic Media-video med en URL-adress lägger du till `VideoPlayer.ssl` i URL-adressen. Om du till exempel vill framtvinga en säker videoleverans lägger du till `&VideoPlayer.ssl=on` i slutet av följande exempel på visningsprogrammets URL:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/VideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&VideoPlayer.ssl=on
   ```

   Se även [Länka URL:er till ditt webbprogram](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Om du publicerar en Dynamic Media-video med inbäddad kod lägger du till `VideoPlayer.ssl` i listan över andra parametrar för visningsprogramkonfiguration i det inbäddade kodfragmentet. Om du till exempel vill tvinga HTTPS-videoleverans lägger du till `&VideoPlayer.ssl=on` som i följande exempel:

   ```
   <style type="text/css"> 
    #s7video_div.s7videoviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/VideoViewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7videoviewer = new s7viewers.VideoViewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/Video", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
      "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
    }).init(); 
   </script>
   ```

   Se även [Bädda in videon på en webbsida](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

