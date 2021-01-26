---
description: Förutom att ändra storlek (size=) och placera (pos=) lager i förhållande till lager 0 och ange kompositionsordningen (z-ordningen) med kommandot layer= kan lager roteras (rotate=) och vändas (flip=).
seo-description: Förutom att ändra storlek (size=) och placera (pos=) lager i förhållande till lager 0 och ange kompositionsordningen (z-ordningen) med kommandot layer= kan lager roteras (rotate=) och vändas (flip=).
seo-title: Lageråtgärder
solution: Experience Manager
title: Lageråtgärder
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a9ef4199-cfa2-480e-a4de-8a0b9064a649
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Lageråtgärder{#layer-operations}

Förutom att ändra storlek (size=) och placera (pos=) lager i förhållande till lager 0 och ange kompositionsordningen (z-ordningen) med kommandot layer= kan lager roteras (rotate=) och vändas (flip=).

Attributen `origin=` och `anchor=` kan användas för att bibehålla den önskade justeringen mellan lager när bilder eller text ändras dynamiskt i mallar.

Kommandot `maskUse=` är tillgängligt för bildlager för att komma åt bakgrundsområdet för bilder som har separata masker.

`opac=` kan användas för att variera lageropaciteten och  `hide=` för att visa eller dölja lagret.
