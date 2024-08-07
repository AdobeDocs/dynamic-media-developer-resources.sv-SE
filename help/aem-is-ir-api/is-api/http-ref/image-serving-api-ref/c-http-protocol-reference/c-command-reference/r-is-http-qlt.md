---
title: qlt
description: JPEG-kvalitet. Anger kodningsattribut för JPEG för att styra komprimeringsnivån. Detta varierar i sin tur filstorleken (mängden svarsdata) och, indirekt, den resulterande bildens visuella kvalitet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# qlt{#qlt}

JPEG-kvalitet. Anger kodningsattribut för JPEG för att styra komprimeringsnivån. Detta varierar i sin tur filstorleken (mängden svarsdata) och, indirekt, den resulterande bildens visuella kvalitet.

` qlt= *`quality`*[, *`chroma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> kvalitet </span> </p> </td> 
  <td class="stentry"> <p>JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> kroma </span> </p> </td> 
  <td class="stentry"> <p>Nedsampling av färgvärden i JPEG (0=normal, 1=inaktiverad); valfritt, standardvärdet är 0. </p> </td> 
 </tr> 
</table>

Högre *`quality`*-värden ökar filstorleken och kvaliteten, lägre värden minskar filstorleken och minskar den upplevda bildkvaliteten. Värden över 90 genererar ofta bilder som inte kan särskiljas från den okomprimerade bilden.

Ställ in flaggan *`chroma`* för att inaktivera nedsampling av kromaticitet i RGB som används av typiska JPEG-kodare. Detta kan öka den upplevda skärpan på kanterna i en bild när kanten definieras av en nyansändring i stället för intensitet. Om du anger den här flaggan kan filstorleken öka något. Experimentera med den här inställningen om texten ser något suddig ut.

## Egenskaper {#section-925a44cbdc9042db8d4eb149cd073d21}

Begär attribut. Används oavsett aktuell lagerinställning. Ignoreras om utdatabildens filformat inte stöder kodning i JPEG. Läs beskrivningen av `fmt=` om du vill ha information om vilka utdatabildformat som stöder `qlt=`.

*`chroma`* ignoreras om utdatapixeltypen är CMYK eller grå.

## Standard {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Exempel {#section-d7d33871d401433aa51d028823eae7a9}

Minska kvaliteten för snabbare överföring via en anslutning med låg bandbredd:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Högre kvalitet för anslutningar med hög bandbredd:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Se även {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
