---
description: Lager placeras genom att lagerorigo (origin=) justeras mot bakgrundslagrets origo vid en förskjutning som anges med pos=.
seo-description: Lager placeras genom att lagerorigo (origin=) justeras mot bakgrundslagrets origo vid en förskjutning som anges med pos=.
seo-title: Lagerplacering
solution: Experience Manager
title: Lagerplacering
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# Lagerplacering{#layer-placement}

Lager placeras genom att lagerorigo (origin=) justeras mot bakgrundslagrets origo vid en förskjutning som anges med pos=.

Om lagerorigo inte anges explicit för ett bildlager beräknas den på följande sätt:

1. Ange bildankarpunkten. Använd `anchor=` eller, om inget anges, `catalog::Anchor`.
1. Om bildankarpunkten är definierad använder du lageromformningarna och `extend=` för att konvertera den till ett origin=-värde.
1. Om ingen bildfästpunkt är definierad placeras lagerstartpunkten i mitten av lagerrektangeln (efter att du har använt `extend=`).

![](assets/layerplacement.png)

