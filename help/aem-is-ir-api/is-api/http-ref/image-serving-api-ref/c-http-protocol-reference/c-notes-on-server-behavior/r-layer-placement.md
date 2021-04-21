---
description: Lager placeras genom att lagerorigo (origin=) justeras mot bakgrundslagrets origo vid en förskjutning som anges med pos=.
solution: Experience Manager
title: Lagerplacering
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# Lagerplacering{#layer-placement}

Lager placeras genom att lagerorigo (origin=) justeras mot bakgrundslagrets origo vid en förskjutning som anges med pos=.

Om lagerorigo inte anges explicit för ett bildlager beräknas den på följande sätt:

1. Ange bildankarpunkten. Använd `anchor=` eller, om inget anges, `catalog::Anchor`.
1. Om bildankarpunkten är definierad använder du lageromformningarna och `extend=` för att konvertera den till ett origin=-värde.
1. Om ingen bildfästpunkt är definierad placeras lagerstartpunkten i mitten av lagerrektangeln (efter att du har använt `extend=`).

![](assets/layerplacement.png)

