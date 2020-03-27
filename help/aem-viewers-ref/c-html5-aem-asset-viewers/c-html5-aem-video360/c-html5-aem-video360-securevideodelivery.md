---
description: 'null'
seo-description: 'null'
seo-title: HTTPS-videoleverans
solution: Experience Manager
title: HTTPS-videoleverans
topic: Dynamic media
uuid: 68984ba1-2802-496a-8ad0-ba46b59514ad
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365

---


# HTTPS-videoleverans{#https-video-delivery}

>[!NOTE]
>
>HTTP Secure Video Delivery gäller endast AEM 6.2 med installation av [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) och AEM 6.1 med installation av [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Förutsatt att visningsprogrammet fungerar i den konfiguration som beskrivs i början av det här avsnittet, kan publicerad videoleverans ske både i HTTPS-läge (säkert) och HTTP-läge (osäkert). I en standardkonfiguration följer leveransprotokollet strikt leveransprotokollet för inbäddningswebbsidan. Det går dock att tvinga fram HTTPS-video utan hänsyn till det protokoll som används när webbsidan bäddas in med [konfigurationsattributet Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md) . (Observera att förhandsgranskning av video i redigeringsläge alltid levereras säkert via HTTPS.)

Beroende på vilken metod du använder för att publicera Dynamic Media-video i AEM används konfigurationsattributet på ett annat sätt, vilket visas i följande exempel: `Video360Player.ssl`

* Om du publicerar en Dynamic Media-video med en URL-adress lägger du till `Video360Player.ssl` URL-adressen. Om du till exempel vill framtvinga en säker videoutgång lägger du `&Video360Player.ssl=on` till slutet av följande exempel på visningsprogramwebbadress:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   Se även [Länka URL:er till ditt webbprogram](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Om du publicerar en Dynamic Media-video med inbäddad kod lägger du till i listan med andra parametrar för visningskonfiguration i kodfragmentet för inbäddning. `Video360Player.ssl` Om du till exempel vill tvinga fram HTTPS-video lägger du till `&Video360Player.ssl=on` följande exempel:

   ```
   <style type="text/css"> 
    #s7video_div.s7video360viewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7video360viewer = new s7viewers.Video360Viewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "Video360Player.ssl" : "on", 
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

   Se även [Bädda in videon på en webbsida](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html)

