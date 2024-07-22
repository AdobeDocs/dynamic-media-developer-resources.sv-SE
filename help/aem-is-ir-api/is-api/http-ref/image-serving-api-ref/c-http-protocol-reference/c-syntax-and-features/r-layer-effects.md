---
title: Lagereffekter
description: Skugg- och glödeffekter av Photoshop-typ implementeras med hjälp av särskilda underlager (effektlager) som kan kopplas till vilket lager som helst (det överordnade lagret), inklusive layer=0 och layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Lagereffekter{#layer-effects}

Skugg- och glödeffekter av Photoshop-typ implementeras med hjälp av särskilda underlager (effektlager) som kan kopplas till vilket lager som helst (det överordnade lagret), inklusive layer=0 och layer=comp.

Effektlager har stöd för ett antal standardattribut och -kommandon för bilder och lager, men är inte avsedda att vara allmänna lager och stöder inte oberoende bild- eller textdata.

Du kan lägga till valfritt antal lagereffekter i ett enda överordnat lager.

## Inre och yttre effekter {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Inre effekter* återges ovanpå det överordnade lagret och visas bara i ogenomskinliga områden i det överordnade lagret. *Yttre effekter* återges bakom det överordnade lagret (så de syns aldrig i ogenomskinliga områden i det överordnade lagret) och kan placeras var som helst i den sammansatta arbetsytan. En inre eller yttre effekt väljs genom att ett positivt eller negativt effektskiktnummer tilldelas med kommandot `effect=`. Kommandot `effect=` styr också z-ordningen för flera effektlager som är kopplade till samma överordnade lager.

## Relation till överordnat lager {#section-eb8bfc4f754a42fc973b562821d6f2d3}

Effektlagren storleksändras automatiskt och placeras så att de sammanfaller med det överordnade lagret (det vill säga effektlagret ärver det överordnade lagrets `size=`- och `origin=`-värden). `pos=` kan användas för att flytta effektlagret bort från det överordnade lagret, vilket vanligtvis krävs för effekter med skugga och inre skugga. För standardlager anger `pos=` en förskjutning mellan det här lagrets ursprung och lagret 0, medan för effektlager `pos=` anger förskjutningen mellan originalen för effektlagret och det överordnade lagret.

## Kommandon och attribut som stöds {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

Effektlager har följande kommandon och attribut:

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

Alla andra bild- och lagerkommandon i effektlagren ignoreras.

## Standardeffektmakron {#section-a01e8dcc87c94495b54a6dfb21d2a718}

För att underlätta användningen av lagereffekter innehåller IS två makron med standardbildkatalogen, `$shadow$` och `$glow$`, som tillhandahåller standardvärden för effektlagerattribut som liknar Photoshop-lagereffekter. I följande tabell visas vilket effektkommando och makro som ska användas för att implementera standardlagereffekterna. Alla attribut som anges i makrona kan ändras i URL-adressen, eller alternativa makron kan skapas för att implementera anpassade lagereffekter.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Önskad effekt </b> </th> 
   <th class="entry"> <b> Kommando</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Skugga </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Inre skugga </p> </td> 
   <td> <p> <span class="codeph"> effekt=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Ytterglöd </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Innerglöd </p> </td> 
   <td> <p> <span class="codeph"> effekt=1&amp;$glöd$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-4c449fdf707b43858917fb271fa1fe96}

Lägg till en tre pixlar bred, röd kant med 50 % opacitet i ett lager:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

Kanten följer konturerna för bildens alfakanal eller mask. Om du ställer in `effect=1` placeras kanten på insidan i stället.

Lägg till en blå skugga i en bild med standardeffektinställningarna (förutom för färgen):

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` lägger till en liten marginal i bildens nedre högra kanter, vilket förhindrar att skuggan klipps ur till bildens gränser.

## Se även {#section-1acccccf534549aea23d4c008c17e7c0}

[effekt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [Kommandomakron%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
