---
description: Lager placeras genom att lagerorigo (origin=) justeras mot bakgrundslagrets origo vid en förskjutning som anges med pos=.
seo-description: Lager placeras genom att lagerorigo (origin=) justeras mot bakgrundslagrets origo vid en förskjutning som anges med pos=.
seo-title: Lagerplacering
solution: Experience Manager
title: Lagerplacering
topic: Scene7 Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Lagerplacering{#layer-placement}

Lager placeras genom att lagerorigo (origin=) justeras mot bakgrundslagrets origo vid en förskjutning som anges med pos=.

Om lagerorigo inte anges explicit för ett bildlager beräknas den på följande sätt:

1. Ange bildankarpunkten. Använd `anchor=`eller, om inget anges, `catalog::Anchor`.
1. Om bildankarpunkten är definierad använder du lageromformningarna och konverterar den `extend=` till ett origin=-värde.
1. Om ingen bildfästpunkt är definierad placeras lagerstartpunkten i mitten av lagerrektangeln (efter användning av `extend=`).

![](assets/layerplacement.png)

