---
description: Anger taggordlistevärden för ett befintligt taggfält.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# setTagFieldValues{#settagfieldvalues}

Anger taggordlistevärden för ett befintligt taggfält.

Syntax

## Auktoriserade användartyper {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-a05cbee4cb4f44198c414a6b14e69156}

**Indata**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| `*`fieldHandle`*` | `xsd:string` | Ja | Fälthandtag för tagg. |
| `*`valueArray`*` | `types:StringArray` | Ja | En array med taggvärden som ersätter fältets befintliga ordlista. Resursassociationer behålls när ett nytt värde matchar ett befintligt värde. |

**Utdata (setTagFieldValuesReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-b11cafd9bed54ab5836c737cc075c918}

**Begäran**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**Svar**

Ingen.
