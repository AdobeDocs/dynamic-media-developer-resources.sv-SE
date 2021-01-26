---
description: Lägger till nya taggvärden i ordlistan för ett befintligt taggfält.
solution: Experience Manager
title: addTagFieldValues
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# addTagFieldValues{#addtagfieldvalues}

Lägger till nya taggvärden i ordlistan för ett befintligt taggfält.

Syntax

## Auktoriserade användartyper {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Indata (addTagFieldValuesParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget för det företag som innehåller taggfältet. |
| `*`fieldHandle`*` | `xsd:string` | Ja | Handtaget för det taggfält som ska ändras. |
| `*`valueArray`*` | `xsd:string` | Ja | En array med taggvärden som ska läggas till i fältets befintliga ordlista. |

**Utdata (addTagFieldValuesParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-c4049392f1c548f883b8b1f8f167bada}

**Begäran**

```java
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**Svar**

Ingen.
