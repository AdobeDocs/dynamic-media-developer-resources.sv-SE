---
description: Returnerar en array med Photoshop sökvägsnamn för den angivna bilden.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# getPhotoshopPathNames{#getphotoshoppathnames}

Returnerar en array med Photoshop sökvägsnamn för den angivna bilden.

Syntax

## Auktoriserade användartyper {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-605a4aab23104489a21f7f7f5849801b}

**Indata (getPhotoshopPathNamesParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Hantera till det företag som innehåller den bild du vill arbeta med. |
| `*`assetHandle`*` | `xsd:string` | Ja | Hantera bildresursen. |

**Utdata (getPhotoshopPathNamesReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`pathNameArray`*` | `types:StringArray` | Ja | En array med Photoshop sökvägsnamn i en bild. |

## Exempel {#section-6d316f14b4184d42af4ca3f717b042dd}

**Begäran**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**Svar**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```

