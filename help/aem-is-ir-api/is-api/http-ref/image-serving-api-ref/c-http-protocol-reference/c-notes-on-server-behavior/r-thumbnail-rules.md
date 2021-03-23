---
description: Tänk på dessa miniatyrregler.
seo-description: Tänk på dessa miniatyrregler.
seo-title: Miniatyrregler
solution: Experience Manager
title: Miniatyrregler
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# Miniatyrregler{#thumbnail-rules}

Tänk på dessa miniatyrregler.

1. Om `catalog::ThumbType=Crop` skalas (beskuren) bilden till minsta möjliga storlek samtidigt som den täcker hela målrektangeln. Om `catalog::ThumbType=Fit` skalas (beskuren) bilden till den största möjliga storleken medan hela bilden fortfarande passas in i målrektangeln. Om `catalog::ThumbType=Texture` skalas (beskuren) bilden till förhållandet `catalog::ThumbRes` till `catalog::Resolution`.
1. Justera den skalförändrade bilden mot målrektangeln baserat på `attribute::ThumbHorizAlign` och `attribute::ThumbVertAlign`.
1. Beskär resultatet till målrektangeln.

