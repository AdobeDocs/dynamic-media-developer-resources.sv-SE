---
description: Tilldela eller uppdatera resurser i ett projekt.
seo-description: Tilldela eller uppdatera resurser i ett projekt.
seo-title: setProjectAssets
solution: Experience Manager
title: setProjectAssets
topic: Scene7 Image Production System API
uuid: 98d18948-d387-4890-9c27-e8ab60cded1d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setProjectAssets{#setprojectassets}

Tilldela eller uppdatera resurser i ett projekt.

Syntax

## Auktoriserade användartyper {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Indata (setProjectAssetsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Ja | Företagshandtag. |
| ` *`projectHandle`*` | `xsd:string` | Ja | Projektreferens. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Ja | Arrayen med resurshandtag som du vill associera med projektet. |

**Utdata (setProjectAssetsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Antalet resurser som lagts till. |

## Exempel {#section-33c1a909c3dc4aa98da474c23a036596}

Det här kodexemplet tilldelar en resurs till ett projekt. Begäran returnerar ett antal lyckade försök.

**Begäran**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**Svar**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```

