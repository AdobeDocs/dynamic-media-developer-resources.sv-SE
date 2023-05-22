---
description: Förutom att ändra storlek (size=) och placera (pos=) lager i förhållande till lager 0 och ange kompositionsordningen (z-ordningen) med kommandot layer= kan lager roteras (rotate=) och vändas (flip=).
solution: Experience Manager
title: Lageråtgärder
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# Lageråtgärder{#layer-operations}

Förutom att ändra storlek (size=) och placera (pos=) lager i förhållande till lager 0 och ange kompositionsordningen (z-ordningen) med kommandot layer= kan lager roteras (rotate=) och vändas (flip=).

The `origin=` och `anchor=` attribut kan användas för att bibehålla den önskade justeringen mellan lager när bilder eller text ändras dynamiskt i mallar.

The `maskUse=` -kommandot är tillgängligt för bildlager för att komma åt bakgrundsområdet för bilder som har separata masker.

`opac=` kan användas för att variera lageropaciteten, och `hide=` om du vill visa eller dölja lagret.
