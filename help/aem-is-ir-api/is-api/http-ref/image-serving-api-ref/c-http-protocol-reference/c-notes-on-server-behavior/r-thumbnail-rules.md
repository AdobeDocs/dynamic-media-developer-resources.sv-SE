---
description: Tänk på dessa miniatyrregler.
solution: Experience Manager
title: Miniatyrregler
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# Miniatyrregler{#thumbnail-rules}

Tänk på dessa miniatyrregler.

1. If `catalog::ThumbType=Crop`, skalas (beskuren) bilden till minsta möjliga storlek samtidigt som den täcker hela målrektangeln. If `catalog::ThumbType=Fit`, skalas (beskuren) bilden till största möjliga storlek samtidigt som hela bilden fortfarande passas in i målrektangeln. If `catalog::ThumbType=Texture`, skalas (beskuren) bilden till proportionerna för `catalog::ThumbRes` till `catalog::Resolution`.
1. Justera den skalförändrade bilden mot målrektangeln baserat på `attribute::ThumbHorizAlign` och `attribute::ThumbVertAlign`.
1. Beskär resultatet till målrektangeln.
