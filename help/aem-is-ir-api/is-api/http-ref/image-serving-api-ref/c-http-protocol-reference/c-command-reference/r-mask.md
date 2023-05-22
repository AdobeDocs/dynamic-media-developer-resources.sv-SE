---
description: Bildmask. Anger en separat maskbild som ska användas som en oassocierad mask.
solution: Experience Manager
title: mask
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# mask{#mask}

Bildmask. Anger en separat maskbild som ska användas som en oassocierad mask.

`mask= *`object`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p></td> 
  <td class="stentry"> <p>Bildobjekt som ska användas som bild- eller lagermask. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Kapslad bildhantering, bildåtergivning eller extern begäran. </p></td> 
 </tr> 
</table>

*`object`* kan vara antingen en katalogpost eller en bild/SVG-fil. Kan anges för bildlager och enfärgade lager.

If *`object`* matchar en bildkatalogspost, `catalog::MaskPath` används, eller `catalog::MaskPath` är inte definierad, sedan `catalog::Path` används. If *`object`* tolkar inte en katalogpost, utan som en filsökväg.

Om källbilden har en alfakanal används den alltid. I annat fall konverteras bilden till gråskala, om det behövs, innan den används som en lagermask.

Om en mask är kopplad till ett enfärgat lager kan den beskäras och skalas med samma regler som används för bilder i bildlager. `size=`, `scale=`, eller `res=` kan användas för att skala masken.

Lagermasker kan också anges i form av en *`nestedRequest`*. Kapslade eller inbäddade begäranden omsluts av klammerparenteser. Förutse en inbäddad bildserverbegäran med `is` och en inbäddad begäran om bildåtergivning med `ir`. En begäran till en extern server antas om inget prefix anges. Se [Begär kapsling och inbäddning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) för mer information.

## Egenskaper {#section-a093043dc249423b8ae322cefb0d545d}

Bild- eller lagerattribut. Gäller för lager 0 om `layer=comp`. Ignoreras av effektlager.

*`object`* får inte matcha en katalogpost som innehåller en `src=` eller `mask=` kommando in `catalog::Modifier`.

The `is` och `ir` -prefix är inte skiftlägeskänsliga.

## Standard {#section-10cf793c665f49deb1b248faa3b618a9}

If `mask=` anges inte uttryckligen och om lagerbilden är kopplad till en katalogpost så anges `catalog::MaskPath` används. I annat fall används alfakanalen för lagerbilden, om sådan finns. Om det inte finns någon alfakanal har lagret ingen mask och lagrets rektangel återges helt ogenomskinlig.

## Exempel {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Använd flera separata masker för att färglägga olika delar av en bild. De färglagda, maskerade områdena läggs ovanpå den ursprungliga, oförändrade bilden:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Se även {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [katalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [Begär kapsling och inbäddning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
