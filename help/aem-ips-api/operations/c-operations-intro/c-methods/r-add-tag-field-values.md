---
description: Lägger till nya taggvärden i ordlistan för ett befintligt taggfält.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '95'
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
