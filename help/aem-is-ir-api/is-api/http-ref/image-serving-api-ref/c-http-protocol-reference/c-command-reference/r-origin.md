---
description: Lagerursprung.
solution: Experience Manager
title: ursprung
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# ursprung{#origin}

Lagerursprung.

`origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>Pixelförskjutning från det övre vänstra hörnet av lagerrektangeln (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Normaliserad förskjutning från mitten av lagerrektangeln (verklig, verklig). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>Lagerrektangeln innehåller alltid ändringar av `extend=`.

Definierar justeringspunkten för lagerrektangeln, som används för att placera lagerrektangeln i förhållande till lager 0 via `pos=`. `originN=0,0` placerar lagerorigo i mitten av lagerrektangeln. `originN=-0.5,-0.5` och  `origin=0,0` är det övre vänstra hörnet och  `originN=0.5,0.5` det nedre högra hörnet av lagerrektangeln.

## Egenskaper {#section-60f639e36ada43d1abc6bfc100afc925}

Lagerattribut. Gäller för det aktuella lagret eller för lagret 0 om `layer=comp`. Påverkas inte av lageromformningar ( `crop=`, `scale=`, `rotate=`, `flip=`) som tillämpas på lagerkällan. Åsidosätter `anchor=`. Ignoreras av effektlager.

## Standard {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Om `origin=` inte anges bestäms lagrets ursprung genom att lageromformningarna tillämpas på bildankarpunkten. Om bildankarpunkten inte är känd används lagerrektangelns mittpunkt ( `originN=0,0`).

## Exempel {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Se Exempel A i [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Se även {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
