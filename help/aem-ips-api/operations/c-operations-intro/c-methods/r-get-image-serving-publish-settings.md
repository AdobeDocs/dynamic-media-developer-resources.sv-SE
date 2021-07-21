---
description: Endast för internt bruk. Användare bör referera till avsnittet Image Serving Image Catalog Reference - Attribute Reference.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
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
