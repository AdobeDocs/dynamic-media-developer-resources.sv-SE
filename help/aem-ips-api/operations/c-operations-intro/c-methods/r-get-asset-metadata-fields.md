---
description: Returnerar alla metadatafält grupperade efter resurstyp.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---

# getAssetMetadataFields{#getassetmetadatafields}

Returnerar alla metadatafält grupperade efter resurstyp.

Syntax

## Auktoriserade användartyper {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**Indata (getAssetMetadataFieldsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Referensen till det företag vars metadata du vill hämta. |

**Utdata (getAssetMetadataFieldsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | Ja | Array med metadatafält, efter resurstyp. |

## Exempel {#section-d79ab85f29144635b0b61416e52f4f3f}

**Begäran**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**Svar**

>[!NOTE]
>
>Trunkerad för att vara snabb.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
