---
description: Omformningar används på källbilder och textlager.
seo-description: Omformningar används på källbilder och textlager.
seo-title: Lageromformningar
solution: Experience Manager
title: Lageromformningar
topic: Scene7 Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Lageromformningar{#layer-transforms}

Omformningar används på källbilder och textlager.

Följande åtgärder tillämpas på källbilder, i den angivna ordningen, för att uppnå det önskade rumsliga förhållandet med lager 0:

1. Använd `crop=`om det anges.
1. Skala baserat på `size=` eller, om `size=` inte anges, baserat på `scale=`eller, om `scale=` inte anges, baserat på `res=`, eller, om `res=`inte anges, använd källbilden med full upplösning.
1. Använd `flip=`om det anges.
1. Använd `rotate=`om det anges.
1. Använd `extend=`om det anges.
1. Placera lagret på arbetsytan baserat på `origin=` och `pos=` (se nedan).

Följande omformningar används på textlager:

1. Textrutans storlek bestäms av `size=`eller textbredden och -höjden, om `size=` endast delvis eller inte alls anges. Texten justeras i textrutan med attributen för rtf-textjustering. Texten kan beskäras av textrutan.
1. Skala textinnehållet baserat på upplösningen som anges med `textAttr=`.
1. Använd `rotate=`om det anges.
1. Använd `extend=`om det anges.
1. Placera lagret på arbetsytan baserat på `origin=` och `pos=`(se nedan).

För både bild- och textlager gäller det sista steget för att placera lagret på arbetsytan inte för lager 0, eftersom lager 0 utgör arbetsytan effektivt.
