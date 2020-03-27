---
description: Bilduppsättning. Anger ett bilduppsättningsvärde som ska användas när req=set-svar genereras.
seo-description: Bilduppsättning. Anger ett bilduppsättningsvärde som ska användas när req=set-svar genereras.
seo-title: imageSet
solution: Experience Manager
title: imageSet
topic: Scene7 Image Serving - Image Rendering API
uuid: ecfb3905-e3ef-4ab8-a2c4-2c3f200e0f0f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# imageSet{#imageset}

Bilduppsättning. Anger ett bilduppsättningsvärde som ska användas när req=set-svar genereras.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Bilduppsättningssträng. </p></td> 
 </tr> 
</table>

Om du vill undvika värdet och se till att inkluderade modifierare inte tolkas som en del av URL-frågesträngen, ska hela värdet omslutas av klammerparenteser. Om katalogposten anges i nätsökvägen åsidosätts det här modifieringsvärdet `catalog::ImageSet` från huvudposten. En beskrivning av giltig syntax för bilduppsättning finns i `catalog::ImageSet` dokumentationen.

## Egenskaper {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Begär attribut. Valfritt. Åsidosätter `catalog::ImageSet` från huvudpost.

## Standard {#section-e8622ff40408450fb79d028f8d37fa6b}

Ingen.

## Exempel {#section-68513d3c601f477399602a0741dab390}

Ange bilduppsättning för användning med `req=set` begäran:

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Se även {#section-7e0320b2e09d475897082711a8f023a9}

[katalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) , [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Media Set Requests](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
