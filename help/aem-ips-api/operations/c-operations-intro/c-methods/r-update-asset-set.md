---
description: Uppdaterar en resursuppsättning.
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# updateAsset{#updateassetset}

Uppdaterar en resursuppsättning.

Syntax

## Parametrar {#section-d7080ccd97334c94860eb107a3e132b2}

**Indata (updateAssetSetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget som innehåller den bilduppsättning som du vill ändra. |
| `*`assetHandle`*` | `xsd:string` | Ja | Handtaget till den bilduppsättning som du vill ändra. |
| `*`setDefinition`*` | `xsd:string` | Nej | Återställer bilduppsättningsmedlemmar. |
| `*`thumbAssetHandle`*` | `xsd:string` | Nej | Handtaget för resursen som fungerar som miniatyrbild för bilduppsättningen. |

**Utdata (updateAssetSetReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
|  |  |  |  |

## Exempel {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Begäran**

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**Svar**

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

