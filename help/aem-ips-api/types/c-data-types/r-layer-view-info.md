---
description: Egenskaper för lagervisning.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '54'
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

