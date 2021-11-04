---
title: HTTP-videoleverans
description: HTTP-videoleverans
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# HTTP-videoleverans{#http-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Om visningsprogrammet fungerar i den konfiguration som beskrivs i början av det här avsnittet, kan publicerad videoleverans ske både i HTTPS-läge (säkert) och HTTP-läge (osäkert). I en standardkonfiguration följer leveransprotokollet strikt leveransprotokollet för inbäddningswebbsidan. Det är dock möjligt att tvinga HTTPS-video att levereras utan hänsyn till det protokoll som används när webbsidan bäddas in med [SmartCropVideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) konfigurationsattribut. (Förhandsgranskning av video i redigeringsläge levereras alltid säkert via HTTPS.)

Beroende på hur du publicerar Dynamic Media-video i Adobe Experience Manager kan `SmartCropVideoPlayer.ssl` konfigurationsattributet används på ett annat sätt, vilket visas i följande exempel:

* Om du publicerar en Dynamic Media-video med en URL-adress lägger du till `SmartCropVideoPlayer.ssl` till webbadressen. Om du till exempel vill framtvinga säker leverans av video lägger du till `&SmartCropVideoPlayer.ssl=on` till slutet av följande exempel på visningsprogramwebbadress:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/SmartCropVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&SmartCropVideoPlayer.ssl=on
   ```

   Se även [Länka URL:er till ditt webbprogram](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Om du publicerar en Dynamic Media-video med inbäddad kod lägger du till `SmartCropVideoPlayer.ssl` till listan över andra konfigurationsparametrar för visningsprogrammet i kodfragmentet för inbäddning. Om du till exempel vill tvinga fram HTTPS-video lägger du till `&SmartCropVideoPlayer.ssl=on` som i följande exempel:

   ```
   <style type="text/css"> 
    #s7video_div.s7videoviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7videoviewer = new s7viewers.SmartCropVideoViewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "SmartCropVideoPlayer.ssl" : "on", 
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

   Se även [Bädda in videon på en webbsida](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
