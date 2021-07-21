---
description: Endast för internt bruk. Se avsnittet Referens-Katalogattribut för bildåtergivning.
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '79'
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
