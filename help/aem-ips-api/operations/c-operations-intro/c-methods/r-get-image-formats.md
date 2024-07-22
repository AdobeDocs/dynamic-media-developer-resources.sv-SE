---
description: Returnerar bildformat som PDF, EPS, SWF med flera.
solution: Experience Manager
title: getImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# getImageFormat{#getimageformats}

Returnerar bildformat som PDF, EPS, SWF med flera.

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
| companyHandle | `xsd:string` | Ja | Handtaget till företaget med de bildformat som du vill ha. |

**Utdata (getImageFormatsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | Ja | Bildformatsmatrisen. |

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
