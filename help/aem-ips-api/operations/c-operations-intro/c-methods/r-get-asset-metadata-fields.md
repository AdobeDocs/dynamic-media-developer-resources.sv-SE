---
description: Returnerar alla metadatafält grupperade efter resurstyp.
seo-description: Returnerar alla metadatafält grupperade efter resurstyp.
seo-title: getAssetMetadataFields
solution: Experience Manager
title: getAssetMetadataFields
topic: Scene7 Image Production System API
uuid: 01d5076f-f187-4069-b2f2-806fb1d8be84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till det företag vars metadata du vill hämta. |

**Utdata (getAssetMetadataFieldsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | Ja | Array med metadatafält, efter resurstyp. |

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

