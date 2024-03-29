---
description: Hämtar alla taggordlistevärden som definierats för ett eller flera taggfält.
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 12836783-4f9d-41d3-9b42-6e25238d7ed5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# getTagFieldValues{#gettagfieldvalues}

Hämtar alla taggordlistevärden som definierats för ett eller flera taggfält.

Syntax

## Auktoriserade användartyper {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-9ad806e7736e4d51ae42cad185050cf9}

**Indata (getTagFieldValuesReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handtaget för det företag som innehåller taggfältet. |
| fieldHandleArray | `types:HandleArray` | Ja | En array med fältreferenser till taggvärden som du vill returnera. |

**Utdata (getTagFieldValuesReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| fieldArray | `types:TagFieldValuesArray` | Ja | En array med taggvärdena i ordlistan för varje begärt fält. |

## Exempel {#section-4492742614e44bb191a7d397dc1a1407}

**Begäran**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**Svar**

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```
