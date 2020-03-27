---
description: Lägger till en eller flera resurser i ett projekt.
seo-description: Lägger till en eller flera resurser i ett projekt.
seo-title: addProjectAssets
solution: Experience Manager
title: addProjectAssets
topic: Scene7 Image Production System API
uuid: 48abea17-058e-4469-bb16-0abee8ef5214
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Hantera till det företag som är associerat med det aktuella projektet. |
| ` *`projectHandle`*` | `xsd:string` | Ja | Hantera det projekt du lägger till resurser i. |
| ` *`projectHandleArray`*` | `xsd:HandleArray` | Ja | Array med resurser som du lägger till i det aktuella projektet. |

**Utdata (addProjectAssetsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Antalet resurser som lagts till. |
| ` *`warningCount`*` | `xsd:int` | Ja | Antalet varningar som genereras när åtgärden försökte lägga till resurser i ett projekt. |
| ` *`errorCount`*` | `xsd:int` | Ja | Antalet fel som genererades när åtgärden försökte lägga till resurser i ett projekt. |
| ` *`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | Nej | Array med varningar som genereras av resurser när åtgärden försökte lägga till dem i ett projekt. |
| ` *`companyHandle`*` | `xsd:AssetOperationFaultArray` | Nej | Array med fel som genereras av resurser när åtgärden försökte lägga till dem i ett projekt. |

## Exempel {#section-bee5be2402f54cb9a3a02cc07def4135}

I det här exemplet läggs en enskild resurs (som refereras av dess referens) till i en resurshanteringsarray till ett projekt som anges i begäran. Åtgärden slutfördes när svaret `successCount` returneras `1`.

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

