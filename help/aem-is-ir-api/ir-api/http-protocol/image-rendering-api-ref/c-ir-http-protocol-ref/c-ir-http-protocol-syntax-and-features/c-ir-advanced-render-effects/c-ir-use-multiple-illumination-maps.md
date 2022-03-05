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

Upp till tre belysningskartor kan skapas för varje vinjett. Belysningskartan för en återgivningsåtgärd markeras med `illum=` och `gloss=` kommandon.

**Standardmarkering** - Om `illum=` eller `gloss=` Om inget anges används den första genererade belysningskartan (vanligen karta A, även platt).

**Automatisk markering med`gloss=`** - Om `illum=` har inte angetts eller är inställd på `-1`jämför återgivaren den angivna `gloss=` med de glansvärden som är associerade med varje belysningskarta i vinjetteringen. Det väljer belysningskartan vars glansvärde är närmast den angivna `gloss=`.

**Explicit markering med`illum=`** - Om `illum=` anges och anges till `0`, `1`, eller `2`använder återgivaren motsvarande belysningskarta, `gloss=` ignoreras när du väljer belysningskartan.

Om vinjetteringen bara innehåller ett belysningskarta används kartan och ignoreras `illum=` och `gloss=` kommandon.
