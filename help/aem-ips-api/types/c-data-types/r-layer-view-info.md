---
description: Egenskaper för lagervisning.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 0%

---

# LayerViewInfo{#layerviewinfo}

Egenskaper för lagervisning.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| url | `xsd:string` | URL för bildserver som representerar mallen. Kombinationer `urlModifier` och `urlPostAp- plyModifier` fält. |
| urlModifier | `xsd:string` | Protokollkommandon för bildvisning som ska användas före begäran eller `urlPostApplyModifier` kommandon. |
| urlPostApplyModifier | `xsd:string` | Protokollkommandon för bildservning som ska användas efter `urlModifier` och begär kommandon. |
