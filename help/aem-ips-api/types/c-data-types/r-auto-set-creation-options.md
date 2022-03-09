---
description: Skapa skriptlista automatiskt för överföringsjobb. Anta att alla skript som anges för överföringen används på alla överförda resurser.
solution: Experience Manager
title: AutoSetCreationOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e6e969be-0410-4be7-88d6-491d715fd137
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# AutoSetCreationOptions{#autosetcreationoptions}

Skapa skriptlista automatiskt för överföringsjobb. Anta att alla skript som anges för överföringen används på alla överförda resurser.

Syntax

## Parametrar {#section-0302e9238dbc4704914e938f42c881e6}

| Namn | Typ | Beskrivning |
|---|---|---|
| autoSetsArray | `types:HandleArray` | Array med [!DNL PropertySet] -hanterare som definierar skript för automatisk set-generering som används vid överföring. |
