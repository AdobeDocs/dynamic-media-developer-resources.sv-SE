---
description: Gör att du kan beskära till begränsningsramen för en inbäddad namngiven bana. Den här beskärningen ändrar i sin tur storleken på bilden.
solution: Experience Manager
title: cropPathE
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# cropPathE{#croppathe}

Gör att du kan beskära till begränsningsramen för en inbäddad namngiven bana. Den här beskärningen ändrar i sin tur storleken på bilden.

`cropPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Namnet på banan som är inbäddad i lagerkällbilden (endast ASCII). </p> <p> <span class="codeph"><span class="varname"> pathName</span></span> är namnet på en bana som är inbäddad i lagerkällbilden. Banan omformas automatiskt efter behov för att bibehålla den relativa justeringen med bildinnehållet. Om mer än en <span class="codeph"><span class="varname"> pathName</span></span> anges beskärs servern till begränsningsramen för varje bana, en åt gången. Alla <span class="codeph"><span class="varname"> pathName</span></span> som inte hittas i källbilden ignoreras. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Lagerattribut. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager.

`cropPathE=` ignoreras om det inte finns någon bana med det angivna namnet i lagerkällbilden eller om lagerkällan inte är en bild.

## Standard {#section-d1986aa31af14767aeb1b4a57add67f4}

Ingen, utan ytterligare beskärning av lagret.

## Se även {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[beskära](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
