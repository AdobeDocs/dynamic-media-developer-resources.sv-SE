---
description: Vissa program kan kräva en annan belysningskarta för olika typer av material.
solution: Experience Manager
title: Använda flera belysningskartor
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# Använda flera belysningskartor{#using-multiple-illumination-maps}

Vissa program kan kräva en annan belysningskarta för olika typer av material.

Upp till tre belysningskartor kan skapas för varje vinjett. Belysningskartan för en återgivningsåtgärd markeras med kommandona `illum=` och `gloss=`.

**StandardmarkeringOm varken** eller  `illum=`   `gloss=` anges kommer återgivaren att använda den första genererade belysningskartan (vanligen karta A, även platt).

**Automatisk markering med`gloss=`** Om  `illum=` inte anges eller är inställd på -1, jämför renderaren det angivna  `gloss=` värdet med glansvärdena som associeras med varje belysningskarta i vinjetteringen, och väljer den belysningskarta vars glansvärde är närmast det angivna  `gloss=`.

**Explicit markering med`illum=`** Om  `illum=` är angivet och inställt på 0, 1 eller 2 kommer återgivaren att använda motsvarande belysningskarta.  `gloss=` ignoreras när belysningskartan väljs.

Om vinjetteringen bara innehåller ett belysningskarta kommer återgivaren att använda kartan och ignorera kommandona `illum=` och `gloss=`.
