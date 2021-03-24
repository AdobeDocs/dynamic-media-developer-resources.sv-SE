---
description: Ersätter bilddata för en bildresurs.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
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

