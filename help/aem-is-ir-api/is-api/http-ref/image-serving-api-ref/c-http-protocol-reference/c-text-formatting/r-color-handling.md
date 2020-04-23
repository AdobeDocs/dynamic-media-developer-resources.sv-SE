---
description: RTF-specifikationen tillåter RGB-färgvärden som anges med \colortbl. Varje komponent levereras separat med kommandona \red, \green och \blue.
seo-description: RTF-specifikationen tillåter RGB-färgvärden som anges med \colortbl. Varje komponent levereras separat med kommandona \red, \green och \blue.
seo-title: Färghantering
solution: Experience Manager
title: Färghantering
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 341693d69fc414dacf984d66e2eaeba2418e663b

---


# Färghantering{#color-handling}

RTF-specifikationen tillåter RGB-färgvärden som anges med `\colortbl`. Varje komponent levereras separat med kommandona `\red`, `\green`och `\blue` .

Det egna RTF-tilläggskommandot `\cmykcolortbl` gör att du kan ange CMYK-färger, där varje färgkomponent finns med `\cyan`-, `\magenta`- `\yellow`och `\black` -kommandona.

Färgkomponentvärdena för `\colortbl` ligger i intervallet 0 till 255. Komponentvärdena för `\cmykcolortbl` ligger i intervallet 0 till 100.

Med tilläggskommandot RTF `\*\iscolortbl`, som stöds av `textPs=`, kan du ange en färgtabell med standardvärden för bildservrar, med fullständigt stöd för RGB, grått, CMYK och alfa. Den har följande syntax:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* ett eller flera IS-färgvärden, separerade med &#39;;&#39;

Mer än en typ av färgtabell kan anges i samma `text=` - eller `textPs=` RTF-sträng. Varje färgtabell kan ha olika antal poster. Image Serving försöker hitta färger i den här ordningen: `\iscolortbl` före `\cmykcolortbl` (endast om pixeltypen för textlagret är CMYK) före `\colortbl`. Färger konverteras `textPs=` endast korrekt mellan CMYK och RGB, om det behövs (t.ex. när RGB-färger anges men CMYK-utdata krävs). Om det inte finns någon färg för ett visst indexvärde används standardfärgen (svart).

I [färgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) finns en beskrivning av syntaxen för IS-färgvärden.

## Begränsningar {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` stöder inte `\*\iscolortbl`. `textPs=` stöder inte `\cmykcolortbl`.

Färgmarkeringar ignoreras när Photoshop-teckensnitt återges.

## Exempel {#section-0f166bb72bd44479be01131077851142}

Tillåt att tre textfärger styrs med variabler, samtidigt som färgstandardvärdet visas när RTF-strängen öppnas i en vanlig RTF-textredigerare.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
