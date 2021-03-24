---
description: Returnerar bildformat som PDF, EPS, SWF och andra.
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget med de bildformat som du vill ha. |

**Utdata (getImageFormatsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`imageFormatArray`*` | `types:ImageFormatArray` | Ja | Bildformatsmatrisen. |

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

