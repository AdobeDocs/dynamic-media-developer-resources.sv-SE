---
description: ID-översättningskarta. Anger reglerna som används för översättning av generiska bild-ID:n till språkområdesspecifika ID:n.
seo-description: ID-översättningskarta. Anger reglerna som används för översättning av generiska bild-ID:n till språkområdesspecifika ID:n.
seo-title: LocaleMap
solution: Experience Manager
title: LocaleMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 3609a595-2948-43a4-ba8c-fd1a9ea4e26e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# LocaleMap{#localemap}

ID-översättningskarta. Anger reglerna som används för översättning av generiska bild-ID:n till språkområdesspecifika ID:n.

` *``*&#42;['|' *`itemItem`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> artikel</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>Språk-ID (ej skiftlägeskänsligt). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Språksuffix. </p></td> 
 </tr> 
</table>

`LocaleMap` refererar till en  `locId` som kan mappas till valfritt antal  `locSuffix`.

Tomma *`locSuffix`*-värden tillåts. *`locSuffix`* värdena måste sorteras i den ordning som de ska sökas igenom. Den första matchningen returneras.

Image Serving söker igenom *`locId`*-värdena efter en skiftlägeskänslig matchning med `locale=`-värdet som anges i begäran. Om en matchning hittas läggs det första associerade *`locSuffix`*-värdet till i det ursprungliga katalog-ID:t. Om den här katalogposten finns används den, annars provas nästa *`locSuffix`*-värde. Om inget av *`locSuffix`*-värdena matchar en katalogpost returnerar Image Serving ett fel eller en standardbild.

Ett tomt *`locId`*-värde matchar tomma och okända `locale=`-strängar. Detta gör att du kan definiera en standardregel för okända språk.

När detta är aktiverat används ID-översättning på alla id som refererar till bildkataloger och statiska innehållskataloginlägg.

## Egenskaper {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Ett eller flera objekt, avgränsade med |, där varje objekt består av två eller flera, kommaavgränsade strängvärden. *`locId`* och  `locale=` jämförs. Inte skiftlägeskänsligt.

## Se även {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Lokaliseringsstöd, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribut::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
