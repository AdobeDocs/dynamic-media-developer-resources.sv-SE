---
title: Lagerplacering
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Lagerplacering{#layer-placement}

Lager placeras genom att lagerorigo (origin=) justeras mot bakgrundslagrets origo vid en förskjutning som anges med pos=.

Om lagerorigo inte anges explicit för ett bildlager beräknas den på följande sätt:

1. Ange bildankarpunkten. Använd `anchor=`eller, om inget anges, `catalog::Anchor`.
1. Om bildankarpunkten är definierad kan du använda lageromformningar och `extend=` för att konvertera den till ett origin=-värde.
1. Om ingen bildfästpunkt har definierats placeras lagerstartpunkten i mitten av lagerrektangeln (efter användning av `extend=`).

![Lagerplaceringsbild](assets/layerplacement.png)
