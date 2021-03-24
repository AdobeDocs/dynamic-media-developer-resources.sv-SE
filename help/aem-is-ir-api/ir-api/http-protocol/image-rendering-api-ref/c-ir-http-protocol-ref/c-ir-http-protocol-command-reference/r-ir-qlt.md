---
description: JPEG-kvalitet. Anger JPEG-kodningsattribut som styr komprimeringsnivån.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# qlt{#qlt}

JPEG-kvalitet. Anger JPEG-kodningsattribut som styr komprimeringsnivån.

` qlt= *``*[. *`kvalitetkroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> kvalitet  </span> </p> </td> 
  <td class="stentry"> <p>JPEG-kodningskvalitet (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> kroma  </span> </p> </td> 
  <td class="stentry"> <p>Nedsampling av färgvärden för JPEG (0=normal, 1=inaktiverad); valfritt, standardvärdet är 0. </p> </td> 
 </tr> 
</table>

Anger JPEG-kodningsattribut som styr komprimeringsnivån. Detta varierar i sin tur filstorleken (mängden svarsdata) och, indirekt, den resulterande bildens visuella kvalitet.

Högre *`quality`*-värden ökar filstorleken och kvaliteten, lägre värden minskar filstorleken och minskar den upplevda bildkvaliteten. Värden över 90 genererar ofta bilder som inte kan särskiljas från den okomprimerade bilden.

Ställ in flaggan *`chroma`* för att inaktivera nedsampling av kromaticitet som används av typiska JPEG-kodare. Detta kan öka den upplevda skärpan på kanterna i en bild när kanten definieras av en nyansändring i stället för intensitet. Om du anger den här flaggan kan filstorleken öka något. Experimentera med den här inställningen om texten ser något suddig ut.

## Egenskaper {#section-897b61c786dd4230a2c5807f2f40e722}

Kan förekomma var som helst i begäran.

Ignoreras om utdatabildformatet inte stöder JPEG-komprimering. Se beskrivningen av `fmt=` för en lista över de utdataformat som stöder JPEG-komprimering.

## Standard {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Se även {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [attribut::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
