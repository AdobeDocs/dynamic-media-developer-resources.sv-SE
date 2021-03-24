---
description: Steg 2 i bildlagrets omformningar ändras enligt följande för miniatyrbilder (t.ex. om req=tmb).
solution: Experience Manager
title: Skalning av miniatyrbilder
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Skalning av miniatyrbilder{#thumbnail-scaling}

Steg 2 i bildlagrets omformningar ändras enligt följande för miniatyrbilder (t.ex. om req=tmb).

* `2.` Om du  `size=` anger det passas bilden (den beskurna) in i  `size=` rektangeln med hjälp av miniatyrregler. Om `size=` inte anges, skalar du baserat på `res=` eller, om `res=` inte anges, anpassar du (beskuren) bilden till arbetsyterektangeln med hjälp av miniatyrreglerna som beskrivs nedan.

