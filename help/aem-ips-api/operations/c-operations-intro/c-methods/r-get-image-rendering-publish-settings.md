---
description: Endast för internt bruk. Se avsnittet Referens-Katalogattribut för bildåtergivning.
seo-description: Endast för internt bruk. Se avsnittet Referens-Katalogattribut för bildåtergivning.
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
topic: Scene7 Image Production System API
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Endast för internt bruk. Se avsnittet Referens-Katalogattribut för bildåtergivning.

Syntax

## Auktoriserade användartyper {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-4f2cb8c589384816bb2525654ec49963}

**Indata (getImageRenderingPublishSettingsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till det företag vars inställningar för bildåtergivning du vill få. |
| ` *`contextHandle`*` | `xsd:string` | Ja | Hantera publiceringskontexten. |

**Utdata (getImageRenderingPublishSettingsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`publishSettingsArray`*` | `type:ConfigSettingArray` | Ja | Publiceringsinställningar för bildåtergivning. |

