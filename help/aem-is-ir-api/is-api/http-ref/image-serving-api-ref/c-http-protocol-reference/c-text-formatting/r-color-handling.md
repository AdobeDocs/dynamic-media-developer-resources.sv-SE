---
description: RTF-specifikationen tillåter RGB-färgvärden som anges med &bsol;colortbl. Varje komponent levereras separat med kommandona &bsol;red, &bsol;green och &bsol;blue.
solution: Experience Manager
title: Färghantering
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Färghantering{#color-handling}

RTF-specifikationen tillåter RGB-färgvärden som anges med `\colortbl`. Varje komponent levereras separat med kommandona `\red`, `\green` och `\blue`.

Med det egna RTF-tilläggskommandot `\cmykcolortbl` kan du ange CMYK-färger, där varje färgkomponent finns i kommandona `\cyan`, `\magenta`, `\yellow` och `\black`.

Färgkomponentvärdena för `\colortbl` ligger i intervallet 0 till 255. Komponentvärdena för `\cmykcolortbl` ligger i intervallet 0 till 100.

Tilläggskommandot för RTF `\*\iscolortbl`, som stöds av `textPs=`, ger ett sätt att ange en färgtabell med standardvärden för bildserverns färg, med fullständigt stöd för RGB, grått, CMYK och alfa. Den har följande syntax:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* ett eller flera IS-färgvärden, separerade med &#39;;&#39;

Mer än en typ av färgtabell kan anges i samma RTF-sträng (`text=`) eller `textPs=`. Varje färgtabell kan ha olika antal poster. Image Serving försöker hitta färger i den här ordningen: `\iscolortbl` före `\cmykcolortbl` (endast om pixeltypen för textlagret är CMYK) före `\colortbl`. Endast för `textPs=` konverteras färger korrekt mellan CMYK och RGB, om det behövs (t.ex. när RGB-färger anges men CMYK-utdata krävs). Om det inte finns någon färg för ett visst indexvärde används standardfärgen (svart).

I [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) finns en beskrivning av syntaxen för IS-färgvärden.

## Begränsningar {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` stöder inte  `\*\iscolortbl`. `textPs=` stöder inte  `\cmykcolortbl`.

Färgmarkeringar ignoreras när Photoshop-teckensnitt återges.

## Exempel {#section-0f166bb72bd44479be01131077851142}

Tillåt att tre textfärger styrs med variabler, samtidigt som färgstandardvärdet visas när RTF-strängen öppnas i en vanlig RTF-textredigerare.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
