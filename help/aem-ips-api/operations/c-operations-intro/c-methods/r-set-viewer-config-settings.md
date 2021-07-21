---
description: Kopplar visningsprogramkonfigurationsinställningar till en resurs. Dessa kan vara en visningsförinställning eller källresurs för visningsprogrammet.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,visningsförinställningar
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '110'
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
