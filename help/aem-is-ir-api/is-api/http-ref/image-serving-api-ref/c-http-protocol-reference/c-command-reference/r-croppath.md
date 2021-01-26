---
description: Gör att du kan beskära till begränsningsramen för en inbäddad namngiven bana. Den här beskärningen ändrar i sin tur storleken på bilden.
seo-description: Gör att du kan beskära till begränsningsramen för en inbäddad namngiven bana. Den här beskärningen ändrar i sin tur storleken på bilden.
seo-title: cropPathE
solution: Experience Manager
title: cropPathE
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4689fd20-dfa0-47eb-8184-cd233f1ac088
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# cropPathE{#croppathe}

Gör att du kan beskära till begränsningsramen för en inbäddad namngiven bana. Den här beskärningen ändrar i sin tur storleken på bilden.

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Namnet på banan som är inbäddad i lagerkällbilden (endast ASCII). </p> <p> <span class="codeph"><span class="varname"> pathName är </span></span> namnet på en bana som är inbäddad i lagerkällbilden. Banan omformas automatiskt efter behov för att bibehålla den relativa justeringen med bildinnehållet. Om mer än en <span class="codeph"><span class="varname"> pathName</span></span> anges beskärs servern till begränsningsramen för varje sökväg, en i taget. Alla <span class="codeph"><span class="varname"> pathName</span></span> som inte hittas i källbilden ignoreras. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Lagerattribut. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager.

`cropPathE=` ignoreras om det inte finns någon bana med det angivna namnet i lagerkällbilden eller om lagerkällan inte är en bild.

## Standard {#section-d1986aa31af14767aeb1b4a57add67f4}

Ingen, utan ytterligare beskärning av lagret.

## Se även {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[beskärning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
