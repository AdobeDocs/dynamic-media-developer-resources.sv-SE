---
description: XMP metadata. Returnerar de XMP metadata som är associerade med bilden som anges i sökvägen för begäran.
seo-description: XMP metadata. Returnerar de XMP metadata som är associerade med bilden som anges i sökvägen för begäran.
seo-title: xmp
solution: Experience Manager
title: xmp
topic: Scene7 Image Serving - Image Rendering API
uuid: e1583ffe-531a-4334-b974-72df6fcb14ba
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---


# xmp{#xmp}

XMP metadata. Returnerar de XMP metadata som är associerade med bilden som anges i sökvägen för begäran.

`req=xmp`

Andra kommandon ignoreras. UTF-8-kodning gäller. Svaret formateras som XML med MIME-typen `text/xml`.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::Expiration`.

## Egenskaper {#section-0d26b6a56c844153ae5cea4880370d00}

Begär attribut. Används oavsett aktuell lagerinställning.

## Standard {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

Om URL:en inte innehåller någon bildsökväg eller modifierare:

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Annars `req=img`

## Exempel {#section-34213692deab4a0f9037d5844132ee14}

Fråga efter bildfilsegenskaper.

` http:// *`server`*/myPath/myImage.tif?req=imageprops`

Fråga efter egenskaper för bildkatalog:

` http:// *`server`*/myRootId?req=catalogprops`

Få åtkomst till egenskaperna för en bildkatalogspost från JavaScript på klientsidan som är inbäddad i en HTML-fil:

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

Hämta maskbilden för en viss katalogpost, som skalats till 25 % av den ursprungliga storleken:

` http:// *`server`*/myRootId/myImageId?req=mask&scale=0.25`

Begär en bild i åttondelsstorlek:

` http:// *`server`*/myRootId/myImageId?scl=8`

Detta är samma sak som:

` http:// *`server`*/myRootId/myImageId?req=img&scl=8`

Begär en miniatyrbild av en bild, beroende på de miniatyrattribut som anges i bildkatalogen:

` http:// *`server`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

Skicka ett textmeddelande till serverloggarna:

` http:// *`server`*/myRootId?req=message&message=This%20is%20the%20message`

## Se även {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [katalog::Target](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md),  [katalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md),  [Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f),  [Properties](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9),  [Image Maps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
