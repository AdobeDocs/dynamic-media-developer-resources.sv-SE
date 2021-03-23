---
description: Endast för internt bruk. Användare bör referera till avsnittet Image Serving Image Catalog Reference - Attribute Reference.
seo-description: Endast för internt bruk. Användare bör referera till avsnittet Image Serving Image Catalog Reference - Attribute Reference.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
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

