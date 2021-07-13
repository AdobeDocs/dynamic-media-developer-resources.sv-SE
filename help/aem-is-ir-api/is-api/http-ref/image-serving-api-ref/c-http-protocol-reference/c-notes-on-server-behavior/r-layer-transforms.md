---
description: Omformningar används på källbilder och textlager.
solution: Experience Manager
title: Lageromformningar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Lageromformningar{#layer-transforms}

Omformningar används på källbilder och textlager.

Följande åtgärder tillämpas på källbilder, i den angivna ordningen, för att uppnå det önskade rumsliga förhållandet med lager 0:

1. Använd `crop=` om det anges.
1. Skala baserat på `size=` eller, om `size=` inte anges, baserat på `scale=`, eller, om `scale=` inte anges, baserat på `res=`, eller, om `res=`inte anges, använd den fullständiga upplösningsbilden för källbilden.
1. Använd `flip=` om det anges.
1. Använd `rotate=` om det anges.
1. Använd `extend=` om det anges.
1. Placera lagret på arbetsytan baserat på `origin=` och `pos=` (se nedan).

Följande omformningar används på textlager:

1. Textrutans storlek bestäms av `size=`, eller textbredden och -höjden om `size=` endast delvis eller inte alls anges. Texten justeras i textrutan med attributen för rtf-textjustering. Texten kan beskäras av textrutan.
1. Skala textinnehållet baserat på upplösningen som anges med `textAttr=`.
1. Använd `rotate=` om det anges.
1. Använd `extend=` om det anges.
1. Placera lagret på arbetsytan baserat på `origin=` och `pos=` (se nedan).

För både bild- och textlager gäller det sista steget för att placera lagret på arbetsytan inte för lager 0, eftersom lager 0 utgör arbetsytan effektivt.
