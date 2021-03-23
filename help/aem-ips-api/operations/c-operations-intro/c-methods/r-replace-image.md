---
description: Ersätter bilddata för en bildresurs.
seo-description: Ersätter bilddata för en bildresurs.
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# replaceImage{#replaceimage}

Ersätter bilddata för en bildresurs.

Syntax

## Auktoriserade användartyper {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Indata (replaceImageParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Ja | Handtaget till företaget med den bild som du vill ersätta. |
| `*`assetHandle`*` | `xsd:string` | Ja | Referensen till resursen som du vill ersätta. |
| `*`urlModifier`*` | `xsd:string` | Ja | Image Server-kommandon som genererar nya bilddata. |

**Utdata (replaceImageReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Ja | Hantera den nya resursen. |

## Exempel {#section-cebb93576bde4cb98cb27356ca66783b}

Det här kodexemplet ersätter en bild och tillämpar ett `urlModifier`-värde med ett kommando som anger att bildservern inte kommer att vidta någon åtgärd vid ersättning.

**Begäran**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**Svar**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```

