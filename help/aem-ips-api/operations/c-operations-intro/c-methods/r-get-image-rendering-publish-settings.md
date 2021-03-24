---
description: Endast för internt bruk. Se avsnittet Referens-Katalogattribut för bildåtergivning.
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '81'
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
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget till det företag vars inställningar för bildåtergivning du vill få. |
| `*`contextHandle`*` | `xsd:string` | Ja | Hantera publiceringskontexten. |

**Utdata (getImageRenderingPublishSettingsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | Ja | Publiceringsinställningar för bildåtergivning. |

