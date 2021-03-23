---
description: Returnerar en array med Photoshop sökvägsnamn för den angivna bilden.
seo-description: Returnerar en array med Photoshop sökvägsnamn för den angivna bilden.
seo-title: getPhotoshopPathNames
solution: Experience Manager
title: getPhotoshopPathNames
uuid: d3f1dea5-393b-498e-963d-37a4e38068a2
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '96'
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

