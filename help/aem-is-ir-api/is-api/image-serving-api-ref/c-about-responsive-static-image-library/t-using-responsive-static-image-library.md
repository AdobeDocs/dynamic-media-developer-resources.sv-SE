---
title: Använda bibliotek för responsiv bild
description: Om du vill lägga till ett responsivt bildbibliotek på en webbsida och hantera befintliga bilder med biblioteket utför du följande steg.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Använda bibliotek för responsiv bild{#using-responsive-image-library}

Om du vill lägga till ett responsivt bildbibliotek på en webbsida och hantera befintliga bilder med biblioteket utför du följande steg.

**Använd bibliotek för responsiv bild**

1. I Dynamic Media Classic [skapar du en bildförinställning](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html?lang=sv-SE#image-sizing) om du tänker använda ett responsivt bildbibliotek med förinställningar.

   När du definierar bildförinställningar som används med responsiva bildbibliotek ska du inte använda några inställningar som påverkar bildstorleken, till exempel `wid=`, `hei=` eller `scl=`. Ange inga storleksfält i bildförinställningen. Lämna dem som tomma värden.
1. Lägg till JavaScript-biblioteksfilen på webbsidan.

   Innan du kan använda biblioteks-API måste du ta med `responsive_image.js`. Den här JavaScript-filen finns i undermappen `libs/` i din standarddistribution av IS-Viewer:

   `<s7viewers_root>/libs/responsive_image.js`
1. Konfigurera befintliga bilder.

   Biblioteket läser vissa konfigurationsattribut från en bildinstans som det arbetar med. Definiera attribut innan API-funktionen `s7responsiveImage` anropas för en sådan bild.

   Du bör också placera den befintliga bild-URL:en i attributet `data-src`. Ställ sedan in det befintliga `src`-attributet så att 1x1 GIF-bild är kodad som data-URI. Om du gör det minskar antalet HTTP-begäranden som skickas av webbsidan vid inläsningen. Observera dock att om SEO (sökmotoroptimering) behövs är det bättre att ställa in ett `title`-attribut för bildinstansen.


   Följande är ett exempel på hur du definierar attributet `data-breakpoints` för bilden och använder en 1x1 GIF som är kodad som Data URI:

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

```html {.line-numbers}
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

Det finns två Smart Crop-lägen i AEM 6.4 och Dynamic Media Viewer 5.9:

* **Manuell** - användardefinierade brytpunkter och motsvarande Image Service-kommandon definieras i ett attribut i image-elementet.
* **Smart beskärning** - beräknade renderingar av smarta beskärningar hämtas automatiskt från leveransservern. Den bästa återgivningen väljs med bildelementets körningsstorlek.

Om du vill använda läget för smart beskärning anger du attributet `data-mode` till `smart crop`. Till exempel:

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Det associerade bildelementet skickar en `s7responsiveViewer`-händelse under körningen när brytpunkten ändras.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
