---
description: Uppdaterar konfigurationsinställningarna för SWF-visningsprogrammet.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,visningsförinställningar
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
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
