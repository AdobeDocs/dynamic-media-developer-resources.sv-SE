---
description: Lägger till en eller flera resurser i ett projekt.
solution: Experience Manager
title: addProjectAssets
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# addProjectAssets{#addprojectassets}

Lägger till en eller flera resurser i ett projekt.

Syntax

## Auktoriserade användartyper {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-20d498e971b6466298e60c8a77fc32b2}

**Indata (addProjectAssetsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Hantera till det företag som är associerat med det aktuella projektet. |
| `*`projectHandle`*` | `xsd:string` | Ja | Hantera det projekt du lägger till resurser i. |
| `*`projectHandleArray`*` | `xsd:HandleArray` | Ja | Array med resurser som du lägger till i det aktuella projektet. |

**Utdata (addProjectAssetsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Antalet resurser som lagts till. |
| `*`warningCount`*` | `xsd:int` | Ja | Antalet varningar som genereras när åtgärden försökte lägga till resurser i ett projekt. |
| `*`errorCount`*` | `xsd:int` | Ja | Antalet fel som genererades när åtgärden försökte lägga till resurser i ett projekt. |
| `*`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | Nej | Array med varningar som genereras av resurser när åtgärden försökte lägga till dem i ett projekt. |
| `*`companyHandle`*` | `xsd:AssetOperationFaultArray` | Nej | Array med fel som genereras av resurser när åtgärden försökte lägga till dem i ett projekt. |

## Exempel {#section-bee5be2402f54cb9a3a02cc07def4135}

I det här exemplet läggs en enskild resurs (som refereras av dess referens) till i en resurshanteringsarray till ett projekt som anges i begäran. Åtgärden slutfördes när svaret `successCount` returnerar `1`.

**Begäran**

```java
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Svar**

```java
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```

