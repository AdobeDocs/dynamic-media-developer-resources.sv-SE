---
description: Egenskaper för lagervisning.
seo-description: Egenskaper för lagervisning.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Dynamic Media Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 0%

---


# LayerViewInfo{#layerviewinfo}

Egenskaper för lagervisning.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`url`*` | `xsd:string` | URL för bildserver som representerar mallen. Kombinerar fälten `urlModifier` och `urlPostAp- plyModifier`. |
| `*`urlModifier`*` | `xsd:string` | Protokollkommandon för bildvisning som ska användas före begäran eller `urlPostApplyModifier`-kommandon. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Protokollkommandon för bildvisning som ska användas efter `urlModifier` och begär kommandon. |

