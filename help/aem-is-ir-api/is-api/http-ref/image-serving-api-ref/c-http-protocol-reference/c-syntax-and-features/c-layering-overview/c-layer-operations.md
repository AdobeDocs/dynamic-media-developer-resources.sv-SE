---
description: Förutom att ändra storlek (size=) och placera (pos=) lager i förhållande till lager 0 och ange kompositionsordningen (z-ordningen) med kommandot layer= kan lager roteras (rotate=) och vändas (flip=).
solution: Experience Manager
title: Lageråtgärder
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# Lageråtgärder{#layer-operations}

Förutom att ändra storlek (size=) och placera (pos=) lager i förhållande till lager 0 och ange kompositionsordningen (z-ordningen) med kommandot layer= kan lager roteras (rotate=) och vändas (flip=).

Attributen `origin=` och `anchor=` kan användas för att bibehålla den önskade justeringen mellan lager när bilder eller text ändras dynamiskt i mallar.

Kommandot `maskUse=` är tillgängligt för bildlager för att komma åt bakgrundsområdet för bilder som har separata masker.

`opac=` kan användas för att variera lageropaciteten och  `hide=` för att visa eller dölja lagret.
