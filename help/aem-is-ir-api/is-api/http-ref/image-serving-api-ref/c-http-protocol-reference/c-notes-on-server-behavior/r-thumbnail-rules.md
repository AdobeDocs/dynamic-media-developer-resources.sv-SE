---
description: Tänk på dessa miniatyrregler.
seo-description: Tänk på dessa miniatyrregler.
seo-title: Miniatyrregler
solution: Experience Manager
title: Miniatyrregler
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Miniatyrregler{#thumbnail-rules}

Tänk på dessa miniatyrregler.

1. Om `catalog::ThumbType=Crop` skalas (beskuren) bilden till minsta möjliga storlek samtidigt som den täcker hela målrektangeln. Om `catalog::ThumbType=Fit` skalas (beskuren) bilden till den största möjliga storleken medan hela bilden fortfarande passas in i målrektangeln. Om `catalog::ThumbType=Texture` skalas (beskuren) bilden till förhållandet `catalog::ThumbRes` till `catalog::Resolution`.
1. Justera den skalförändrade bilden mot målrektangeln baserat på `attribute::ThumbHorizAlign` och `attribute::ThumbVertAlign`.
1. Beskär resultatet till målrektangeln.

