---
description: Flyttar en resurs till en viss mapp.
seo-description: Flyttar en resurs till en viss mapp.
seo-title: moveAsset
solution: Experience Manager
title: moveAsset
topic: Scene7 Image Production System API
uuid: cabeb7b7-ab0b-44d0-ad90-623f76e4323d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# moveAsset{#moveasset}

Flyttar en resurs till en viss mapp.

Syntax

## Auktoriserade användartyper {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-dd0bbdf293aa4563af70a91f97c861f1}

**Indata (moveAssetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handla till företaget. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Hantera den resurs du vill flytta. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Hantera målmappen. |

**Utdata (moveAssetReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-78333769f4f14e2886fdf06433c9d2ad}

Det här kodexemplet flyttar en resurs till en mapp.

**Begäran**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**Svar**

Ingen.
