---
description: Kopplar visningsprogramkonfigurationsinställningar till en resurs. Dessa kan vara en visningsförinställning eller källresurs för visningsprogrammet.
seo-description: Kopplar visningsprogramkonfigurationsinställningar till en resurs. Dessa kan vara en visningsförinställning eller källresurs för visningsprogrammet.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: d83d866e-9243-479f-9b33-727aad8158e5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# setViewerConfigSettings{#setviewerconfigsettings}

Kopplar visningsprogramkonfigurationsinställningar till en resurs. Dessa kan vara en visningsförinställning eller källresurs för visningsprogrammet.

Syntax

## Auktoriserade användartyper {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-bcc8c83cc84141e8b1341be9133e8511}

**Indata (setViewerConfigSettingsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handla till företaget. |
| `*`assetHandle`*` | `xsd:string` | Ja | Resurshandtag. |
| `*`name`*` | `xsd:string` | Ja | Resursnamn. |
| `*`type`*` | `xsd:string` | Ja | Den typ av resurs som du vill använda visningsprogramkonfigurationen på. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Ja | Arrayen `ConfigSettings` som används för resursen. |

**Utdata (setViewerConfigSettingsParam)**

IPS API returnerar inget svar för den här åtgärden.
