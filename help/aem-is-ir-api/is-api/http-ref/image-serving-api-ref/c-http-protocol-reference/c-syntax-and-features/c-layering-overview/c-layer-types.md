---
description: Fyra typer av lager stöds.
solution: Experience Manager
title: Lagertyper
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Lagertyper{#layer-types}

Fyra typer av lager stöds.

## Bildlager {#section-3e53df1437694272aca03f927fc0db07}

Bildlager måste ha en `src=` som anger vilken bild som ska användas som lager. En separat bild kan anges med `mask=` som ska användas som lagermask eller bilden redan har en alfakanal. Storleken på bildlager hämtas alltid från bilden, men bilden skalas ofta så att den passar med `size=` -kommando. En klippbana kan användas med `clipPath=`.

## Textlager {#section-dc2aec6416a340bcb20c1f884323c8d0}

Måste ha en `text=` eller `textPs=` som tillhandahåller textinnehållet i form av ett RTF-textfragment (Rich Text Format). Textlager kan ha en egen storlek som är anpassad efter innehållet eller få explicita storlekar. Om texten till exempel ska radbrytas till en viss bredd, eller om texten måste begränsas inom ett visst område. `textPs=` stöd för att flöda text till godtyckliga former som definieras med `textFlowPath=` och på godtyckliga sökvägar som definieras med `textPath=`. `textPs=` stöder även återgivning av text i textrutan eller den angivna formen i godtycklig vinkel ( `textAngle=`).

## Solida färglager {#section-56dfb672756643dda08dc93294809eb0}

Heltäckande färglager används ofta för lager 0 i mallar, så att den sammansatta bildens storlek är fast och oberoende av bildens innehåll. Heltäckande färglager kräver en `color=` och antingen `size=` eller `mask=`och har stöd för de flesta andra kommandon och attribut för att ändra utseendet. Solida färglager kan få godtyckliga former med `clipPath=`.

## Effektlager {#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop-liknande lagereffekter som skuggor och glödeffekter implementeras med IS med hjälp av särskilda underlager som kan bifogas till bild-, text- och heltäckande färglager. Dessa effektlager ärver den överordnade lagermasken och positionen från det överordnade lagret och är begränsade i funktionalitet.
