---
description: Steg 2 i bildlagrets omformningar ändras enligt följande för miniatyrbilder (t.ex. om req=tmb).
solution: Experience Manager
title: Skalning av miniatyrbilder
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# Skalning av miniatyrbilder{#thumbnail-scaling}

Steg 2 i bildlagrets omformningar ändras enligt följande för miniatyrbilder (t.ex. om req=tmb).

* `2.` If `size=` har angetts och anpassar (beskuren) bilden till `size=` rect med hjälp av miniatyrregler. If `size=` har inte angetts, skalas baserat på `res=`, eller om `res=` har inte angetts, anpassa (beskuren) bilden till arbetsyterektangeln med hjälp av miniatyrreglerna som beskrivs nedan.
