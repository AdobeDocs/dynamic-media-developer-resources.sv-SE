---
description: ID-översättningskarta. Anger reglerna som används för översättning av generiska bild-ID:n till språkspecifika ID:n.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# LocaleMap{#localemap}

ID-översättningskarta. Anger reglerna som används för översättning av generiska bild-ID:n till språkspecifika ID:n.

`*`objekt`*&#42;['|' *`objekt`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objekt </span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[',<span class="varname"> locSuffix</span>] </p></td> 
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

`LocaleMap` refererar till en `locId` som kan mappas till valfritt antal `locSuffix`.

Tomma *`locSuffix`* värden tillåts. *`locSuffix`* värden måste sorteras i den ordning som de ska sökas igenom. Den första matchningen returneras.

Image Serving söker igenom *`locId`*-värdena efter en skiftlägesokänslig matchning med det `locale=`-värde som anges i begäran. Om en matchning hittas läggs det första associerade *`locSuffix`*-värdet till i det ursprungliga katalog-ID:t. Om den här katalogposten finns används den, annars provas nästa *`locSuffix`*-värde. Om inget av *`locSuffix`*-värdena matchar en katalogpost returnerar Image Serving ett fel eller en standardbild.

Ett tomt *`locId`*-värde matchar tomma och okända `locale=`-strängar. Detta gör att du kan definiera en standardregel för okända språk.

När detta är aktiverat används ID-översättning på alla id som refererar till bildkataloger och statiska innehållskataloginlägg.

## Egenskaper {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Ett eller flera objekt, avgränsade med |, där varje objekt består av två eller flera, kommaavgränsade strängvärden. *`locId`* och `locale=` jämförs. Inte skiftlägeskänslig.

## Se även {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Lokaliseringsstöd, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
