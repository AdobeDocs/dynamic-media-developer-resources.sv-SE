---
description: Fyra typer av lager stöds.
seo-description: Fyra typer av lager stöds.
seo-title: Lagertyper
solution: Experience Manager
title: Lagertyper
topic: Scene7 Image Serving - Image Rendering API
uuid: d88b2163-7c9f-4885-9722-be3339e7127a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# Lagertyper{#layer-types}

Fyra typer av lager stöds.

## Bildlager {#section-3e53df1437694272aca03f927fc0db07}

Bildlager måste ha ett `src=`-kommando som anger vilken bild som ska användas som lager. En separat bild kan anges med `mask=` som ska användas som lagermask, eller så har bilden redan en alfakanal. Storleken på bildlager hämtas alltid från bilden, men bilden skalas ofta så att den passar med kommandot `size=`. En klippsökväg kan användas med `clipPath=`.

## Textlager {#section-dc2aec6416a340bcb20c1f884323c8d0}

Måste ha ett `text=`- eller `textPs=`-kommando som tillhandahåller textinnehållet i form av ett RTF-textfragment (Rich Text Format). Textlager kan vara självstorleksanpassade efter innehållet eller få explicita storlekar (t.ex. om texten ska radbrytas till en viss bredd eller om texten måste begränsas inom ett visst område). `textPs=` stöder flödning av text till godtyckliga former som definieras med  `textFlowPath=` och till godtyckliga banor som definieras med  `textPath=`. `textPs=` har även stöd för att återge text i textrutan eller i den angivna formen i valfri vinkel (  `textAngle=`).

## Solida färglager {#section-56dfb672756643dda08dc93294809eb0}

Heltäckande färglager används ofta för lager 0 i mallar, så att den sammansatta bildens storlek är fast och oberoende av bildens innehåll. Heltäckande färglager kräver ett `color=`-attribut, antingen `size=` eller `mask=`, och stöder de flesta andra kommandon och attribut för att ändra utseendet. Solida färglager kan få godtyckliga former med `clipPath=`.

## Effektlager {#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop-liknande lagereffekter som skuggor och glödeffekter implementeras med IS med hjälp av särskilda underlager som kan bifogas till bild-, text- och heltäckande färglager. Dessa effektlager ärver den överordnade lagermasken och positionen från det överordnade lagret och är begränsade i funktionalitet.
