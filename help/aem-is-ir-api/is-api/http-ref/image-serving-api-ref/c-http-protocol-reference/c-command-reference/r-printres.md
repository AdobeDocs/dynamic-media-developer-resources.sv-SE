---
description: Utskriftsupplösning. Åsidosätter utskriftsupplösningsvärdet som är inbäddat i svarsbilden.
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# printRes{#printres}

Utskriftsupplösning. Åsidosätter utskriftsupplösningsvärdet som är inbäddat i svarsbilden.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Utskriftsupplösning (dpi). </p></td> 
 </tr> 
</table>

Utskriftsupplösningen definieras normalt av `catalog::PrintResolution` om det är en katalogpost, annars med utskriftsupplösningsvärdet som är inbäddat i källbilden. När det gäller en mallbild eller sammansatt bild med flera lager är standardutskriftsupplösningen som är inbäddad i svarsfilen utskriftsupplösningen för lagerbilden med det lägsta lagernumret.

Om du anger utskriftsupplösningen ändras inte svarsbildens pixelstorlek.

## Egenskaper {#section-03c7910ebe234804a319e5d0d8ef3a74}

Begär attribut. Används oavsett den aktuella lagerinställningen.

## Standard {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` eller den utskriftsupplösning som är inbäddad i källbilden.

## Se även {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[katalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
