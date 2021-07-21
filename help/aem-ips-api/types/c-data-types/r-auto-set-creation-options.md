---
description: Skapa skriptlista automatiskt för överföringsjobb. Anta att alla skript som anges för överföringen används på alla överförda resurser.
solution: Experience Manager
title: AutoSetCreationOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e6e969be-0410-4be7-88d6-491d715fd137
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---

# AutoSetCreationOptions{#autosetcreationoptions}

Skapa skriptlista automatiskt för överföringsjobb. Anta att alla skript som anges för överföringen används på alla överförda resurser.

Syntax

## Parametrar {#section-0302e9238dbc4704914e938f42c881e6}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`autoSetsArray`*` | `types:HandleArray` | En matris med [!DNL PropertySet]-handtag som definierar de skript för automatisk set-generering som används vid överföring. |
