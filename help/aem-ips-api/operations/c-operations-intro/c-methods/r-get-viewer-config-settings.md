---
description: Hämtar alla visningsprogramkonfigurationsinställningar som är associerade med den angivna resursen.
seo-description: Hämtar alla visningsprogramkonfigurationsinställningar som är associerade med den angivna resursen.
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
topic: Scene7 Image Production System API
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '79'
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
| ` *`companyHandle`*` | `xsd:string` | Ja | Handla till företaget. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Hantera tillgången. |

**Utdata (getViewerConfigSettingsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`type`*` | `xsd:string` | Ja | Visningstyp som konfigurationsinställningarna gäller för. |
| ` *`configSettingsArray`*` | `types:ConfigSettingsArray` | Ja | Array med visningsprogrammets konfigurationsinställningar. |

