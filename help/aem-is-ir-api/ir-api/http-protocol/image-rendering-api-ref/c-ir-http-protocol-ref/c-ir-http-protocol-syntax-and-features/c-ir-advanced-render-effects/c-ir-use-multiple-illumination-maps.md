---
title: Använda flera belysningskartor
description: Vissa program kan kräva en annan belysningskarta för olika typer av material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Använda flera belysningskartor{#using-multiple-illumination-maps}

Vissa program kan kräva en annan belysningskarta för olika typer av material.

Upp till tre belysningskartor kan skapas för varje vinjett. Belysningskartan för en återgivningsåtgärd markeras med kommandona `illum=` och `gloss=`.

**Standardmarkering** - Om `illum=` eller `gloss=` inte anges används den första genererade belysningskartan (vanligen karta A, även platt).

**Automatisk markering med`gloss=`** - Om `illum=` inte har angetts eller är inställd på `-1` jämför återgivaren det angivna `gloss=`-värdet med glansvärdena som associeras med varje belysningskarta i vinjetteringen. Den väljer belysningskarta vars glanskvärde är närmast den angivna `gloss=`.

**Explicit markering med`illum=`** - Om `illum=` har angetts och angetts till `0`, `1` eller `2` använder återgivaren motsvarande belysningskarta. `gloss=` ignoreras när belysningskartan väljs.

Om vinjetteringen bara innehåller ett belysningskarta används kartan och kommandona `illum=` och `gloss=` ignoreras.
