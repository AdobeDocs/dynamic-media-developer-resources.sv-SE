---
description: Hämtar användardefinierade metadatafält som är associerade med en resurs.
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# getMetadataFields{#getmetadatafields}

Hämtar användardefinierade metadatafält som är associerade med en resurs.

Syntax

## Auktoriserade användartyper {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-bac949e59c0546429c5786fe422d750d}

**Indata (getMetadataFieldsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Företagets handtag. |
| assetType | `xsd:string` | Ja | Resurstyper som metadata ska hämtas från. |

**Utdata (getMetadataFieldsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| Kodfras | `Code Phrase` |  |  |

## Exempel {#section-dbfde1483d614b5aac2b491cb32115d7}

Detta kodexempel returnerar metadataresurser för den angivna typen och företaget. Svaret innehåller en array med metadatafält i en fältarray. Alla resurser har inte samma metadata. IPS-användaren definierar objektets metadatafält.

**Begäran**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**Svar**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```
