---
description: Hämtar alla visningsprogramkonfigurationsinställningar som är associerade med den angivna resursen.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,visningsförinställningar
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# getViewerConfigSettings{#getviewerconfigsettings}

Hämtar alla visningsprogramkonfigurationsinställningar som är associerade med den angivna resursen.

Syntax

## Auktoriserade användartyper {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-7d06abf3d707494c8a1270c7fa1477f1}

**Indata (getViewerConfigSettingsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handla till företaget. |
| `*`assetHandle`*` | `xsd:string` | Ja | Hantera tillgången. |

**Utdata (getViewerConfigSettingsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`type`*` | `xsd:string` | Ja | Visningstyp som konfigurationsinställningarna gäller för. |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | Ja | Array med visningsprogrammets konfigurationsinställningar. |
