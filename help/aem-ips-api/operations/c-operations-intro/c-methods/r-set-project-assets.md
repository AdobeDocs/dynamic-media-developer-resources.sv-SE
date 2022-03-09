---
description: Tilldela eller uppdatera resurser i ett projekt.
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

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
| companyName | `xsd:string` | Ja | Företagshandtag. |
| projectHandle | `xsd:string` | Ja | Projektreferens. |
| assetHandleArray | `types:HandleArray` | Ja | Arrayen med resurshandtag som du vill associera med projektet. |

**Utdata (setProjectAssetsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Antalet resurser som lagts till. |

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
