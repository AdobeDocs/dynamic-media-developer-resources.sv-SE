---
description: Egenskaper för lagervisning.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

Egenskaper för lagervisning.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| url | `xsd:string` | URL för bildserver som representerar mallen. Kombinerar fälten `urlModifier` och `urlPostAp- plyModifier`. |
| urlModifier | `xsd:string` | Protokollkommandon som ska användas för bildvisning före begäran eller `urlPostApplyModifier` kommandon. |
| urlPostApplyModifier | `xsd:string` | Protokollkommandon för bildvisning som ska användas efter `urlModifier` och begära kommandon. |
