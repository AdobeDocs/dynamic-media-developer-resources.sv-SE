---
description: Sökväg till maskfil. Relativ eller absolut sökväg och namn för en maskbildfil som är associerad med den här katalogposten.
seo-description: Sökväg till maskfil. Relativ eller absolut sökväg och namn för en maskbildfil som är associerad med den här katalogposten.
seo-title: MaskPath
solution: Experience Manager
title: MaskPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a2d1f08a-0a26-41a6-9be2-f5cc2afb15c4
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---


# MaskPath{#maskpath}

Sökväg till maskfil. Relativ eller absolut sökväg och namn för en maskbildfil som är associerad med den här katalogposten.

Tillåter att separata masker kopplas till bilder.

Servern använder de regler för sökvägsupplösning som beskrivs i [Hantera källdata](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) för att hitta datafilen.

## Egenskaper {#section-cdc3b7e2811e41008479cd97887c01b7}

Textsträngsvärde. Valfritt. Om det anges måste det vara en giltig relativ eller absolut sökväg till Image Server-filen. `attribute::DefaultExt` läggs till om det inte finns något filsuffix.

Om både en huvudbild ( `catalog::Path`) och en maskbild ( `catalog::MaskPath`) definieras i en katalogpost måste båda ha exakt samma pixelstorlek. Maskbilder måste vara 8-bitars gråskalebilder.

`mask=` i begäran åsidosätter  `catalog::MaskPath`.

`catalog::MaskPath` åsidosätter alfakanalen i huvudbilden (  `catalog::Path`), om sådan finns, och om alfakanalen inte är associerad (d.v.s. inte förmultiplicerad). Om bildens alfa är förmultiplicerat ignoreras `catalog::MaskPath` och alfakanalen används alltid.

## Standard {#section-78533e35bfec469ba087cb68a35bb81b}

Ingen.

## Se även {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md),  [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c),  [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md),  [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
