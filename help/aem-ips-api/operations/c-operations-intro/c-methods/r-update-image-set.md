---
description: Uppdaterar en bilduppsättning.
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# updateImageSet{#updateimageset}

Uppdaterar en bilduppsättning.

Syntax

## Parametrar {#section-3be47dbbce474ce78676b05e163492e3}

**Indata (updateImageSetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget som innehåller den bilduppsättning som du vill ändra. |
| `*`assetHandle`*` | `xsd:string` | Ja | Handtaget till den bilduppsättning som du vill ändra. |
| `*`memberArray`*` | `types:ImageSetMemberUpdateArray` | Nej | Återställer bilduppsättningsmedlemmar. |
| `*`thumbAssetHandle`*` | `xsd:string` | Nej | Handtaget för resursen som fungerar som miniatyrbild för bilduppsättningen. |

**Utdata (updateImageSetReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`sekvens`*` |  |  |  |

## Exempel {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Begäran**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**Svar**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

