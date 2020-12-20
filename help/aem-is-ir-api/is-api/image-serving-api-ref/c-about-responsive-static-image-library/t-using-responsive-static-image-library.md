---
description: Om du vill lägga till ett responsivt bildbibliotek på en webbsida och hantera befintliga bilder med biblioteket utför du följande steg.
seo-description: Om du vill lägga till ett responsivt bildbibliotek på en webbsida och hantera befintliga bilder med biblioteket utför du följande steg.
seo-title: Använda bibliotek för responsiv bild
solution: Experience Manager
title: Använda bibliotek för responsiv bild
topic: Scene7 Image Serving - Image Rendering API
uuid: 325cdc8d-2bfa-4f9b-bf88-51d1dcc6c495
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---


# Använda responsivt bildbibliotek{#using-responsive-image-library}

Om du vill lägga till ett responsivt bildbibliotek på en webbsida och hantera befintliga bilder med biblioteket utför du följande steg.

**Använda bibliotek för responsiv bild**

1. I SPS skapar [du en bildförinställning](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html) om du planerar att använda ett responsivt bildbibliotek med förinställningar.

   När du definierar förinställningar för bilder som används med ett responsivt bildbibliotek ska du inte använda några inställningar som påverkar bildstorleken, till exempel `wid=`, `hei=` eller `scl=`. Ange inga storleksfält i bildförinställningen. Lämna dem som tomma värden.
1. Lägg till JavaScript-biblioteksfilen på webbsidan.

   Innan du kan använda biblioteks-API måste du ta med `responsive_image.js`. Den här JavaScript-filen finns i undermappen `libs/` i din standarddistribution av IS-Viewers:

   `<s7viewers_root>/libs/responsive_image.js`
1. Konfigurera befintliga bilder.

   Biblioteket läser vissa konfigurationsattribut från en bildinstans som det arbetar med. Definiera attribut innan API-funktionen `s7responsiveImage` anropas för en sådan bild.

   Du bör också placera den befintliga bild-URL:en i attributet `data-src`. Ställ sedan in det befintliga `src`-attributet så att en 1x1 GIF-bild kodas som data-URI. Om du gör det minskar antalet HTTP-begäranden som skickas av webbsidan vid inläsningen. Observera dock att om SEO (sökmotoroptimering) behövs är det bättre att ställa in ett `title`-attribut för bildinstansen.

   Följande är ett exempel på hur du definierar `data-breakpoints`-attributet för bilden och använder en 1x1 GIF-kodad som Data URI:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Anropa API-funktionen `s7responsiveImage` för varje bildinstans som hanteras i biblioteket.

   Anropa API-funktionen `s7responsiveImage` för varje bildinstans som hanteras i biblioteket. Efter ett sådant anrop ersätter biblioteket den ursprungliga bilden med bilden som hämtas från Image Serving enligt körningsstorleken för elementet `IMG` i webbsideslayouten och enhetsskärmens densitet.

   Följande kod är ett exempel på hur API-funktionen `s7responsiveImage` anropas i en bild, förutsatt att `responsiveImage` är ett ID för den bilden:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Exempel {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

Biblioteket har stöd för att arbeta med många bildinstanser på webbsidan samtidigt. Upprepa därför steg 1 och 2 ovan för varje bild som du vill att biblioteket ska hantera.

Det är webbsidans ansvar att formatera bildelementet så att det blir flexibelt i storlek. Det responsiva bildbiblioteket skiljer inte mellan bilder med fast storlek och&quot;flytande&quot; bilder. Om den används på en bild med fast storlek läses den nya bilden in endast en gång.

Följande kod är ett komplett exempel på en enkel webbsida som har en enda flytande bild som hanteras av biblioteket för responsiv bild. Exemplet innehåller extra CSS-format som gör bilden&quot;responsiv&quot; till webbläsarfönstrets storlek:

```
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>
```

**Använda smart beskärning**

Det finns två smarta beskärningslägen i AEM 6.4 och Scene7 Viewer 5.9:

* **Manuella** , användardefinierade brytpunkter och motsvarande Image Service-kommandon definieras i ett attribut i image-elementet.
* **Smart Crop**  - Beräknade renderingar av smarta beskärningar hämtas automatiskt från leveransservern. Den bästa återgivningen väljs med bildelementets körningsstorlek.

Om du vill använda läget för smart beskärning anger du `data-mode`-attributet till `smart crop`. Exempel:

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Det associerade bildelementet skickar en `s7responsiveViewer`-händelse under körning när brytpunkten ändras.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
