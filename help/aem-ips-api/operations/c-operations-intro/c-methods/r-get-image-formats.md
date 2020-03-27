---
description: Returnerar bildformat som PDF, EPS, SWF och andra.
seo-description: Returnerar bildformat som PDF, EPS, SWF och andra.
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
topic: Scene7 Image Production System API
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getImageFormats{#getimageformats}

Returnerar bildformat som PDF, EPS, SWF och andra.

Syntax

## Auktoriserade användartyper {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-eefa36a70b74498f8727ef61d98cfb63}

**Indata (getImageFormatsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget med de bildformat som du vill ha. |

**Utdata (getImageFormatsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`imageFormatArray`*` | `types:ImageFormatArray` | Ja | Bildformatsmatrisen. |

## Exempel {#section-73881e12839b4904bf3299b0920bdd0c}

Det här kodexemplet returnerar alla bildformat för det angivna företaget.

**Begäran**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**Svar**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```

