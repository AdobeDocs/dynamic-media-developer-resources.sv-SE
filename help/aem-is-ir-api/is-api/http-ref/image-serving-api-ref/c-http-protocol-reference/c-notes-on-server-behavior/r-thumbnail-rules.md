---
description: Tänk på dessa miniatyrregler.
seo-description: Tänk på dessa miniatyrregler.
seo-title: Miniatyrregler
solution: Experience Manager
title: Miniatyrregler
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Miniatyrregler{#thumbnail-rules}

Tänk på dessa miniatyrregler.

1. Om `catalog::ThumbType=Crop`så skalas (beskuren) bilden till minsta möjliga storlek samtidigt som hela målrektangeln täcks. Om `catalog::ThumbType=Fit`så skalas (den beskurna) bilden till den största möjliga storleken samtidigt som hela bilden fortfarande passas in i målrektangeln. Om `catalog::ThumbType=Texture`den (beskurna) bilden skalas till förhållandet mellan `catalog::ThumbRes` och `catalog::Resolution`.
1. Justera den skalförändrade bilden mot målrektangeln baserat på `attribute::ThumbHorizAlign` och `attribute::ThumbVertAlign`.
1. Beskär resultatet till målrektangeln.

