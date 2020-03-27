---
description: Konfigurationsattribut definieras som attribut direkt i ett IMG-element som hanteras av biblioteket för responsiv bild. Varje bild kan ha en egen uppsättning attribut.
seo-description: Konfigurationsattribut definieras som attribut direkt i ett IMG-element som hanteras av biblioteket för responsiv bild. Varje bild kan ha en egen uppsättning attribut.
seo-title: Kommandoreferens - Konfigurationsattribut
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
topic: Scene7 Image Serving - Image Rendering API
uuid: a3d52680-2a28-40c8-9b5f-b1c252c88e4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattribut definieras som attribut direkt i ett IMG-element som hanteras av biblioteket för responsiv bild. Varje bild kan ha en egen uppsättning attribut.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Valfritt.

URL till den bild som Image Serving visar. Om URL:en inte finns använder biblioteket det värde som är angivet i attributet som `src` reserv. Det här attributet används för den inledande bilden och den dynamiska bilden som hanteras från olika platser i biblioteket för responsiv bild.

**Exempel**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Om `data-src` är inställt är `src` det valfritt och kan innehålla alla URL-adresser som du vill lägga till. Den kan till exempel innehålla en URL till samma bildserverbaserade bild som används i biblioteket. Eller så kan den innehålla en GIF-platshållare eller till och med en data-URI för att undvika en extra serverrundtur vid start.

Om `data-src` inte anges `src` är obligatoriskt och måste innehålla en URL till den bild som Image Serving visar.

**Exempel**

Använda data-URI för `src` attributet och Image Serving URL för `data-src` attributet:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

En kommaavgränsad lista med brytpunkter och eventuellt följt av ett kolon ( `:`), och kommandot Bildvisning eller Bildförinställningar. Varje brytpunkt är ett bildbreddsvärde som definieras i logiska CSS-pixlar. Biblioteket läser in bilden med det närmaste större värdet från listan och nedskalar den på klienten för att matcha CSS-bildbredden vid körning. (Om du arbetar på en skärm med hög densitet representerar bildåtergivningar som läses in från servern brytpunktsvärden som multipliceras med enhetens pixelförhållande.)

För varje brytpunkt i listan är det möjligt att definiera ett eller flera bildserverskommandon eller förinställningsnamn. Sådana extra parametrar tillämpas bara på bilden om den här brytpunkten är aktiv.

Du kan använda vilket bildserverkommando som helst som stöds, förutom de kommandon som påverkar svarsbildens storlek, som `wid=`, `hei=`eller `scl=`. Samma begränsning gäller för bildförinställningar: en bildförinställning som används med ett responsivt bildbibliotek får inte innehålla sådana kommandon.

Kommandon för flera bildservrar eller bildförinställningsnamn avgränsas med tecknet &quot; `&`&quot;. Om ett bildserverkommando har ett kommatecken i värdet ersätts det med `%2C`. Namn på bildförinställningar omsluts av dollartecken ( `$`).

**Exempel**

**Använda endast brytpunkter**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Använda bildserverskommandon**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Använda bildförinställningar**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Använda förinställda bilder och bildserverkommandon**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## dataläge {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Följande två smarta beskärningslägen är tillgängliga i AEM 6.4 och senare samt i Scene7 Viewer 5.9 och senare:

* **Manuella** - användardefinierade brytpunkter och motsvarande bildtjänstkommandon definieras i ett attribut i bildelementet.
* **Smart Crop** - Beräknade renderingar av smarta beskärningar hämtas automatiskt från leveransservern. Den bästa återgivningen väljs med bildelementets körningsstorlek.

Om du vill använda läget för smart beskärning anger du attributet `data-mode` till `smart crop`.

**Exempel**

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Det associerade bildelementet skickar en `s7responsiveViewer` händelse under körning när brytpunkten ändras.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```

