---
description: Konfigurationsattribut definieras som attribut direkt i ett IMG-element som hanteras av biblioteket för responsiv bild. Varje bild kan ha en egen uppsättning attribut.
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattribut definieras som attribut direkt i ett IMG-element som hanteras av biblioteket för responsiv bild. Varje bild kan ha en egen uppsättning attribut.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Valfritt.

URL till den bild som Image Serving visar. Om URL:en inte finns använder biblioteket värdet som är angivet i attributet `src` som reserv. Det här attributet används för den inledande bilden och den dynamiska bilden som hanteras från olika platser i biblioteket för responsiv bild.

**Exempel**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```


## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Om `data-src` anges är `src` valfritt och kan innehålla alla URL-adresser som du vill lägga till. Den kan till exempel innehålla en URL till samma bildserverbaserade bild som används i biblioteket. Eller så kan den innehålla en GIF-platshållare eller till och med en data-URI för att undvika en extra serverrundtur vid start.

Om `data-src` inte anges är `src` obligatoriskt och måste innehålla en URL till den bild som Image Serving visar.


**Exempel**

Använder data-URI för attributet `src` och Image Serving URL för attributet `data-src`:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```


## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

En kommaavgränsad lista med brytpunkter och eventuellt följt av ett kolon ( `:`), kommandona Bildvisning eller Bildförinställningar. Varje brytpunkt är ett bildbreddsvärde som definieras i logiska CSS-pixlar. Biblioteket läser in bilden med det närmaste större värdet från listan och nedskalar den på klienten för att matcha CSS-bildbredden vid körning. (Om du arbetar på en skärm med hög densitet representerar bildåtergivningar som läses in från servern brytpunktsvärden som multipliceras med enhetens pixelförhållande.)

För varje brytpunkt i listan är det möjligt att definiera ett eller flera bildserverskommandon eller bildförinställningsnamn. Sådana extra parametrar tillämpas bara på bilden om den här brytpunkten är aktiv.

Du kan använda vilket bildserverkommando som helst, förutom de kommandon som påverkar svarsbildens storlek, som `wid=`, `hei=` eller `scl=`. Samma begränsning gäller för bildförinställningar: en bildförinställning som används med ett responsivt bildbibliotek får inte innehålla sådana kommandon.

Kommandon för flera bildservrar eller namn på bildförinställningar avgränsas med tecknet `&`. Om ett bildserverkommando har ett kommatecken i värdet ersätts det med `%2C`. Namn på bildförinställningar omsluts av dollartecken ( `$`).


**Exempel**

**Använder bara brytpunkter**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Använda bildserverkommandon**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Använda bildförinställningar**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Använda kommandona Bildförinställningar och Bildvisning**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`



## dataläge {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Följande två Smart Crop-lägen är tillgängliga i AEM 6.4 och senare samt i Dynamic Media Viewer 5.9 och senare:

* **Manuell** - användardefinierade brytpunkter och motsvarande Image Service-kommandon definieras i ett attribut i image-elementet.
* **Smart beskärning** - beräknade renderingar av smarta beskärningar hämtas automatiskt från leveransservern. Den bästa återgivningen väljs med bildelementets körningsstorlek.

Om du vill använda läget för smart beskärning anger du attributet `data-mode` till `smart crop`.

**Exempel**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Det associerade bildelementet skickar en `s7responsiveViewer`-händelse under körningen när brytpunkten ändras.

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
