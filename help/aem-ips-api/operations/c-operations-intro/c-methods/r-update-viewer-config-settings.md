---
description: Uppdaterar konfigurationsinställningarna för SWF-visningsprogrammet.
seo-description: Uppdaterar konfigurationsinställningarna för SWF-visningsprogrammet.
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '65'
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
