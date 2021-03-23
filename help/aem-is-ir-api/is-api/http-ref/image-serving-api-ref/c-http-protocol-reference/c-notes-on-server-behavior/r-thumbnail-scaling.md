---
description: Steg 2 i bildlagrets omformningar ändras enligt följande för miniatyrbilder (t.ex. om req=tmb).
seo-description: Steg 2 i bildlagrets omformningar ändras enligt följande för miniatyrbilder (t.ex. om req=tmb).
seo-title: Skalning av miniatyrbilder
solution: Experience Manager
title: Skalning av miniatyrbilder
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Skalning av miniatyrbilder{#thumbnail-scaling}

Steg 2 i bildlagrets omformningar ändras enligt följande för miniatyrbilder (t.ex. om req=tmb).

* `2.` Om du  `size=` anger det passas bilden (den beskurna) in i  `size=` rektangeln med hjälp av miniatyrregler. Om `size=` inte anges, skalar du baserat på `res=` eller, om `res=` inte anges, anpassar du (beskuren) bilden till arbetsyterektangeln med hjälp av miniatyrreglerna som beskrivs nedan.

