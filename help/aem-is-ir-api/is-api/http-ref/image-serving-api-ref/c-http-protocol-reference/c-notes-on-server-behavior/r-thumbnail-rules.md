---
description: Tänk på dessa miniatyrregler.
solution: Experience Manager
title: Miniatyrregler
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Miniatyrregler{#thumbnail-rules}

Tänk på dessa miniatyrregler.

1. Om `catalog::ThumbType=Crop` skalas (beskuren) bilden till minsta möjliga storlek samtidigt som den täcker hela målrektangeln. Om `catalog::ThumbType=Fit` skalas (beskuren) bilden till den största möjliga storleken medan hela bilden fortfarande passas in i målrektangeln. Om `catalog::ThumbType=Texture` skalas (beskuren) bilden till förhållandet `catalog::ThumbRes` till `catalog::Resolution`.
1. Justera den skalförändrade bilden mot målrektangeln baserat på `attribute::ThumbHorizAlign` och `attribute::ThumbVertAlign`.
1. Beskär resultatet till målrektangeln.

