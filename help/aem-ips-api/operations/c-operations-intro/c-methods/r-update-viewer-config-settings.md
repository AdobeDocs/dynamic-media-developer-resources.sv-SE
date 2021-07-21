---
description: Uppdaterar konfigurationsinställningarna för SWF-visningsprogrammet.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,visningsförinställningar
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

Uppdaterar konfigurationsinställningarna för SWF-visningsprogrammet.

Syntax

## Auktoriserade användartyper {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-29790d933fb24aa392d0cb2d52d1310f}

**Indata (updateViewerConfigSettingsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handla till företaget. |
| `*`assetHandle`*` | `xsd:string` | Ja | Resurshandtag. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Ja | Array med konfigurationsinställningar som du vill använda för visningsprogrammet. |

**Utdata (updateViewerConfigSettingsReturn)**

IPS API returnerar inget svar för den här åtgärden.
