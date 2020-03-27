---
description: Anger taggordlistevärden för ett befintligt taggfält.
seo-description: Anger taggordlistevärden för ett befintligt taggfält.
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
topic: Scene7 Image Production System API
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| ` *`fieldHandle`*` | `xsd:string` | Ja | Fälthandtag för tagg. |
| ` *`valueArray`*` | `types:StringArray` | Ja | En array med taggvärden som ersätter fältets befintliga ordlista. Resursassociationer behålls när ett nytt värde matchar ett befintligt värde. |

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
