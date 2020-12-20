---
description: Steg 2 i bildlagrets omformningar ändras enligt följande för miniatyrbilder (t.ex. om req=tmb).
seo-description: Steg 2 i bildlagrets omformningar ändras enligt följande för miniatyrbilder (t.ex. om req=tmb).
seo-title: Skalning av miniatyrbilder
solution: Experience Manager
title: Skalning av miniatyrbilder
topic: Scene7 Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# Skalning av miniatyrbilder{#thumbnail-scaling}

Steg 2 i bildlagrets omformningar ändras enligt följande för miniatyrbilder (t.ex. om req=tmb).

* `2.` Om du  `size=` anger det passas bilden (den beskurna) in i  `size=` rektangeln med hjälp av miniatyrregler. Om `size=` inte anges, skalar du baserat på `res=` eller, om `res=` inte anges, anpassar du (beskuren) bilden till arbetsyterektangeln med hjälp av miniatyrreglerna som beskrivs nedan.

