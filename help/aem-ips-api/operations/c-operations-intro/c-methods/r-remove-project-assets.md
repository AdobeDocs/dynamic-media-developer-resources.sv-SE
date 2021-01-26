---
description: Tar bort resurser från ett projekt. Förstör inte tillgångarna.
seo-description: Tar bort resurser från ett projekt. Förstör inte tillgångarna.
seo-title: removeProjectAssets
solution: Experience Manager
title: removeProjectAssets
topic: Dynamic Media Image Production System API
uuid: bae09dc3-4328-4264-8fb2-e4f0c53546eb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# removeProjectAssets{#removeprojectassets}

Tar bort resurser från ett projekt. Förstör inte tillgångarna.

Syntax

## Auktoriserade användartyper {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-169d8e317417415b87df86242f65710e}

**Indata (removeProjectAssetsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget med de resurser som du vill flytta. |
| `*`projectHandle`*` | `xsd:string` | Ja | Referensen till de projektresurser som du vill flytta. |
| `*`assetHandleArray`*` | `types:HandleArray` | Ja | En array med handtag till de resurser du vill flytta. |

**Utdata (removeProjectAssetsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Antal resurser har tagits bort. |
| `*`warningCount`*` | `xsd:int` | Ja | Antalet varningar som genereras när åtgärden försökte ta bort resurser från projektet. |
| `*`errorCount`*` | `xsd:int` | Ja | Antalet fel som genererades när åtgärden försökte ta bort resurser från projektet. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade varningar när åtgärden försökte ta bort dem från projektet. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade fel när åtgärden försökte ta bort dem från projektet. |

## Exempel {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Detta kodexempel tar bort 2 resurser från ett projekt (anges av projektreferensen).

**Begäran**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```

