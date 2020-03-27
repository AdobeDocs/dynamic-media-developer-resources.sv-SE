---
description: Markera objekt efter pixelplats.
seo-description: Markera objekt efter pixelplats.
seo-title: sel
solution: Experience Manager
title: sel
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a679284-9da4-44b6-b495-8e1a47296e7c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sel{#sel}

Markera objekt efter pixelplats.

` sel= *``*, *``*[, *`xynivå`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>Välj platskoordinater i pixlar (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nivå </span> </p> </td> 
  <td class="stentry"> <p>Gruppnivå (int). </p> </td> 
 </tr> 
</table>

Markerar gruppen eller objektet vid de pixelkoordinater som anges av *`x, y`* och startar ett nytt MSS. Om inget markeringsbart objekt finns på plockplatsen, eller om plockplatsen inte är giltig, `attribute::OnFailSel` utförs åtgärden som anges av.

*`level`* anger om den yttersta gruppen ska markeras eller om detaljnivån ska göras i en kapslad grupp eller ett kapslat objekt. Om *`level`* inte anges markeras den yttersta gruppen. Ange 1 om du vill välja en gruppnivå under den yttersta gruppen. Ange ett stort tal (till exempel 99) för att markera det innersta objekt eller den grupp som kan markeras.

## Egenskaper {#section-8f27e84d88734a62a5e398e0c9972bdc}

Markeringskommando; MSS-avgränsare. Objektmarkeringen är beständig tills ett annat objekt markeras, antingen med `obj=` eller `sel=`.

*`x, y`* måste ligga i intervallet 0, 0 (bildens övre vänstra hörn) till *`wid`*-1, *`hei`*-1 (bildens nedre högra hörn), där *`wid`* och *`hei`* är storleken på den ej skalade vinjetteringsvyn.

Om det anges *`level`* måste det vara 0 eller större.

## Standard {#section-e13c705a3e76468894b4ec190ed8a893}

Inget för *`x, y`*. *`level`* är som standard 0.

## Se även {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribut::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribut::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
