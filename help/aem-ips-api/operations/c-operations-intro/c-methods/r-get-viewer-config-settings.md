---
description: Hämtar alla visningsprogramkonfigurationsinställningar som är associerade med den angivna resursen.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,visningsförinställningar
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '77'
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

