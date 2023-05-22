---
description: RTF-specifikationen tillåter färgvärden för RGB som anges med &bsol;colortbl. Varje komponent levereras separat med kommandona &bsol;red, &bsol;green och &bsol;blue.
solution: Experience Manager
title: Färghantering
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Färghantering{#color-handling}

RTF-specifikationen tillåter färgvärden för RGB som anges med `\colortbl`. Varje komponent levereras separat med `\red`, `\green`och `\blue` kommandon.

Det egna RTF-tilläggskommandot `\cmykcolortbl` gör att du kan ange CMYK-färger, där varje färgkomponent som ingår i `\cyan`, `\magenta`, `\yellow`och `\black` kommandon.

Färgkomponentvärden för `\colortbl` ligger mellan 0 och 255. Komponentvärden för `\cmykcolortbl` ligger mellan 0 och 100.

Kommandot RTF-tillägg `\*\iscolortbl`, stöds av `textPs=`I finns ett sätt att ange en färgtabell med standardvärden för bildservrar, med stöd för RGB, grått, CMYK och alfa. Den har följande syntax:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* ett eller flera IS-färgvärden, separerade med &#39;;&#39;

Fler än en typ av färgtabell kan anges i samma `text=` eller `textPs=` RTF-sträng. Varje färgtabell kan ha olika antal poster. Image Serving försöker hitta färger i den här ordningen: `\iscolortbl` före `\cmykcolortbl` (endast om pixeltypen för textlagret är CMYK) före `\colortbl`. För `textPs=` bara färger konverteras korrekt mellan CMYK och RGB, om det behövs (t.ex. när RGB-färger anges men CMYK-utdata krävs). Om det inte finns någon färg för ett visst indexvärde används standardfärgen (svart).

Se [färg](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) för en beskrivning av syntaxen för IS-färgvärden.

## Begränsningar {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` stöder inte `\*\iscolortbl`. `textPs=` stöder inte `\cmykcolortbl`.

Färgmarkeringar ignoreras när Photoshop-teckensnitt återges.

## Exempel {#section-0f166bb72bd44479be01131077851142}

Tillåt att tre textfärger styrs med variabler, samtidigt som färgstandardvärdet visas när RTF-strängen öppnas i en vanlig RTF-textredigerare.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
