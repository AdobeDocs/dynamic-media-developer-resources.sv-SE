---
title: Färghantering
description: RTF-specifikationen tillåter färgvärden för RGB som anges med &bsol;colortbl. Varje komponent levereras separat med kommandona &bsol;red, &bsol;green och &bsol;blue.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Färghantering{#color-handling}

RTF-specifikationen tillåter färgvärden för RGB som anges med `\colortbl`. Varje komponent tillhandahålls separat med kommandona `\red`, `\green` och `\blue`.

Det egna RTF-tilläggskommandot `\cmykcolortbl` gör det möjligt att ange CMYK-färger, där varje färgkomponent finns i kommandona `\cyan`, `\magenta`, `\yellow` och `\black`.

Färgkomponentvärdena för `\colortbl` ligger i intervallet 0-255. Komponentvärdena för `\cmykcolortbl` ligger i intervallet 0-100.

RTF-tilläggskommandot `\*\iscolortbl`, som stöds av `textPs=`, erbjuder ett sätt att ange en färgtabell med standardfärgvärden för bildservrar, med stöd för RGB, grått, CMYK och alfa. Den har följande syntax:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* ett eller flera IS-färgvärden, separerade med &#39;;&#39;

Mer än en typ av färgtabell kan anges i samma `text=`- eller `textPs=` RTF-sträng. Varje färgtabell kan ha olika antal poster. Bildservning försöker hitta färger i den här ordningen: `\iscolortbl` före `\cmykcolortbl` (endast om pixeltypen för textlagret är CMYK) före `\colortbl`. Endast för `textPs=` konverteras färger korrekt mellan CMYK och RGB, om det behövs (t.ex. när RGB-färger har angetts men CMYK-utdata krävs). Om det inte finns någon färg för ett visst indexvärde används standardfärgen (svart).

I [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) finns en beskrivning av syntaxen för IS-färgvärden.

## Begränsningar {#section-c5173e672d854e4aa9656844f7fc4d0e}

Modifieraren `text=` stöder inte `\*\iscolortbl`. Modifieraren `textPs=` stöder inte `\cmykcolortbl`.

Färgmarkeringar ignoreras när Photoshop-teckensnitt återges.

## Exempel {#section-0f166bb72bd44479be01131077851142}

Tillåt att tre textfärger styrs med variabler, samtidigt som färgstandardvärdet visas när RTF-strängen öppnas i en vanlig RTF-textredigerare.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
