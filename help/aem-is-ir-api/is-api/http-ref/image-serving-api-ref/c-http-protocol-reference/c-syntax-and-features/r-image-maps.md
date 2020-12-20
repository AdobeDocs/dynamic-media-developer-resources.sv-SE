---
description: IS innehåller mekanismer för att förenkla användningen av HTML-bildscheman. De JAVA-baserade och Flash-baserade visningsprogrammen i IS har också begränsat stöd för bildscheman.
seo-description: IS innehåller mekanismer för att förenkla användningen av HTML-bildscheman. De JAVA-baserade och Flash-baserade visningsprogrammen i IS har också begränsat stöd för bildscheman.
seo-title: Bildscheman
solution: Experience Manager
title: Bildscheman
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---


# Bildscheman{#image-maps}

IS innehåller mekanismer för att förenkla användningen av HTML-bildscheman. De JAVA-baserade och Flash-baserade visningsprogrammen i IS har också begränsat stöd för bildscheman.

Källbildscheman tillhandahålls till IS antingen via `catalog::Map` eller med kommandot `map=`, och bearbetade kartor hämtas med kommandot `req=map`.

Ett bildschema består av ett eller flera HTML AREA-element som är rätt avgränsade med &#39;&lt;&#39; och &#39;>&#39;. Om det anges via katalog::Map antas alla pixelkoordinatvärden vara i den ursprungliga bildupplösningen och i förhållande till det övre vänstra hörnet i (oförändrad) källbilden. När koordinatvärdena anges via ett `map=`-kommando antas de vara lagerkoordinater i förhållande till lagrets övre vänstra hörn (efter `rotate=` och `extend=`).

>[!NOTE]
>
>% koordinater tillåts inte för närvarande och kan behandlas felaktigt.

IS genererar ett sammansatt bildschema från källbildscheman för varje ingående lager genom att tillämpa de spatiala omformningarna (t.ex. skalning och rotation) på kartkoordinaterna och sedan sätta ihop de bearbetade lagermappningarna i lämplig z-ordning (framsida till baksida) och med lämplig placering.

Följande kommandon används för bearbetning av bildscheman i samband med `req=map` (antingen direkt i begäran, via katalogmallar eller i `catalog::Modifier`-strängar):

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

Attributen `SHAPE` och `COORDS` för en `AREA` kan ändras under bearbetning av en `req=map`-begäran. Alla andra attribut för `AREA`-elementet skickas utan ändring. I de flesta fall innebär detta att du ändrar `SHAPE`-värdet från `DEFAULT` till `RECT` (detta lägger även till attributet `COORDS`) eller ändrar `COORDS`-värdena.

Alla `AREA`-element som blir tomma under bearbetningen tas bort helt. Om en karta är associerad med `layer=comp` placeras den bakom alla andra kartor. Data returneras i text från ett eller flera HTML `AREA`-element. En tom svarssträng anger att det inte finns något bildschema för de angivna objekten.

Lagergenomskinlighet beaktas inte vid kartbearbetning. Ett helt genomskinligt lager kan fortfarande ha ett bildschema kopplat till sig. Kartan för ett delvis genomskinligt lager klipps inte bort till de genomskinliga områdena.

## Se även {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [katalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md),  [HTML 4.01 Specification](http://www.w3.org/TR/html401/)
