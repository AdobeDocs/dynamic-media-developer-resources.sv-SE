---
description: Endast för internt bruk. Användare bör referera till avsnittet Image Serving Image Catalog Reference - Attribute Reference.
seo-description: Endast för internt bruk. Användare bör referera till avsnittet Image Serving Image Catalog Reference - Attribute Reference.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
topic: Dynamic Media Image Production System API
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

Endast för internt bruk. Användare bör referera till avsnittet Image Serving Image Catalog Reference - Attribute Reference.

Syntax

## Auktoriserade användartyper {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-79f0d54acd604ad2a5c96679334f2424}

**Indata (getImageServingPublishSettingsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget med bilden som visar publiceringsinställningar. |
| `*`contextHandle`*` | `xsd:string` | Ja | Hantera publiceringskontexten. |

**Utdata**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | Ja | Array med bildserverns publiceringsinställningar. |

