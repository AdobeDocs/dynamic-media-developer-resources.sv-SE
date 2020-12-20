---
description: Beskär bild. Anger ett rektangulärt beskärningsområde, uttryckt antingen i pixlar eller normaliserat i förhållande till den högupplösta källbilden eller maskbilden.
seo-description: Beskär bild. Anger ett rektangulärt beskärningsområde, uttryckt antingen i pixlar eller normaliserat i förhållande till den högupplösta källbilden eller maskbilden.
seo-title: beskära
solution: Experience Manager
title: beskära
topic: Scene7 Image Serving - Image Rendering API
uuid: c8eca467-7564-48a6-82d7-17f68a1399e1
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---


# beskär{#crop}

Beskär bild. Anger ett rektangulärt beskärningsområde, uttryckt antingen i pixlar eller normaliserat i förhållande till den högupplösta källbilden eller maskbilden.

`crop= *``*, *`kodstorlek`*`

`cropN= *``*, *`coordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>Pixelförskjutning från källbildens övre vänstra hörn till det övre vänstra hörnet av beskärningsrektangeln (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Normaliserad förskjutning från det övre vänstra hörnet i källbilden till det övre vänstra hörnet i beskärningsrektangeln (reellt, reellt). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p></td> 
  <td class="stentry"> <p>Beskärningsrektangelns storlek i pixlar (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Normaliserad storlek på beskärningsrektangeln i förhållande till källbildens storlek (verklig, verklig). </p></td> 
 </tr> 
</table>

Kan även användas för att utöka bilden utanför gränserna genom att ange negativa x-, y-värden och/eller bredd, höjdvärden som är större än bildens bredd, höjd. I det här fallet är det utökade området helt genomskinligt (om inte `bgColor=` har angetts).

## Egenskaper {#section-632e0405bb9940679b5f8b1c10e0902e}

Källbild/maskattribut. Gäller för källbilden för lagret 0 om `layer=comp`. Ignoreras av lager som inte är kopplade till en källbild eller källmask.

## Standard {#section-41f62d386c664f77952bc22e7286bb88}

Hela bilden ( `cropN=0,0,1,1`).

## Exempel {#section-2c99b481c0a04321979a3b522aa295d1}

**Beskär 10 % från vänster och 10 % från höger:**

`…&cropN=0.1,0,0.8,1&…`

**Beskär 20 % från en bilds nederkant:**

`…&cropN=0,0,1,0.8&…`

## Se även {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [cropPathbgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
