---
description: Hämtar unika metadatafältvärden.
seo-description: Hämtar unika metadatafältvärden.
seo-title: getUniqueMetadataValues
solution: Experience Manager
title: getUniqueMetadataValues
topic: Scene7 Image Production System API
uuid: 5b2f95a7-cc0b-4938-99b9-2aefa0ffe693
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---


# getUniqueMetadataValues{#getuniquemetadatavalues}

Hämtar unika metadatafältvärden.

Syntax

## Auktoriserade användartyper {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-b9d1413811c24566b6d095701f0f66db}

**Indata (getUniqueMetadataValuesParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handla till företaget. |
| ` *`fieldHandle`*` | `xsd:string` | Nej | Hantera till metadatafält. |

**Utdata (getUniqueMetadataValuesReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`values`*` | `type:StringArray` |  |  |

## Exempel {#section-440f3bc3e5be436cb6ec26117d05f476}

I det här kodexemplet används en fältreferens för att returnera specifika metadatavärden.

**Begäran**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**Svar**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```

