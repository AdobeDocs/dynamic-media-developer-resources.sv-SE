---
description: IS innehåller mekanismer för att förenkla användningen av bildscheman för HTML. De JAVA-baserade och Flash-baserade visningsprogrammen i IS har också begränsat stöd för bildscheman.
solution: Experience Manager
title: Bildscheman
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Bildscheman{#image-maps}

IS innehåller mekanismer för att förenkla användningen av bildscheman för HTML. De JAVA-baserade och Flash-baserade visningsprogrammen i IS har också begränsat stöd för bildscheman.

Källbildscheman tillhandahålls till IS antingen via `catalog::Map` eller med `map=` och bearbetade kartor hämtas med `req=map` -kommando.

Ett bildschema består av ett eller flera HTML AREA-element, som är rätt avgränsade med &#39;&lt;&#39; och &#39;>&#39;. Om det anges via katalog::Map antas alla pixelkoordinatvärden vara i den ursprungliga bildupplösningen och i förhållande till det övre vänstra hörnet i (oförändrad) källbilden. När det tillhandahålls via en `map=` -kommandot antas koordinatvärdena vara lagerkoordinater i förhållande till lagrets övre vänstra hörn (efter `rotate=` och `extend=`).

>[!NOTE]
>
>% koordinater tillåts inte för närvarande och kan behandlas felaktigt.

IS genererar ett sammansatt bildschema från källbildscheman för varje ingående lager genom att tillämpa de spatiala omformningarna (t.ex. skalning och rotation) på kartkoordinaterna och sedan sätta ihop de bearbetade lagermappningarna i lämplig z-ordning (framsida till baksida) och med lämplig placering.

Följande kommandon används för bearbetning av bildscheman när de finns tillsammans med `req=map` (antingen direkt i begäran, via katalogmallar eller i `catalog::Modifier` strängar):

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

Alla andra kommandon ignoreras.

The `SHAPE` och `COORDS` attribut för en `AREA` kan ändras under bearbetning av en `req=map` request, all other attributes of the `AREA` -elementet skickas utan ändring. I de flesta fall innebär detta att `SHAPE` värde från `DEFAULT` till `RECT` (det skulle också innebära att `COORDS` attribut), eller ändra `COORDS` värden.

Alla `AREA` element som blir tomma under bearbetningen tas bort helt. Om en karta är associerad med `layer=comp` den placeras bakom alla andra kartor. Data returneras i textform en som eller flera HTML `AREA` -element. En tom svarssträng anger att det inte finns något bildschema för de angivna objekten.

Lagergenomskinlighet beaktas inte vid kartbearbetning. Ett helt genomskinligt lager kan fortfarande ha ett bildschema kopplat till sig. Kartan för ett delvis genomskinligt lager klipps inte bort till de genomskinliga områdena.

## Se även {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [katalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [Specifikation för HTML 4.01](https://www.w3.org/TR/html401/)
