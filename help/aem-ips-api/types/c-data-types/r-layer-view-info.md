---
description: Egenskaper för lagervisning.
seo-description: Egenskaper för lagervisning.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Scene7 Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LayerViewInfo{#layerviewinfo}

Egenskaper för lagervisning.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| ` *`url`*` | `xsd:string` | URL för bildserver som representerar mallen. Kombinerar `urlModifier` och `urlPostAp- plyModifier` fält. |
| ` *`urlModifier`*` | `xsd:string` | Protokollkommandon för bildvisning som ska användas före begäran eller `urlPostApplyModifier` kommandon. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Protokollkommandon för bildvisning som ska användas efter `urlModifier` och begära kommandon. |

