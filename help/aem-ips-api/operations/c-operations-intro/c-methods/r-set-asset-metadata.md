---
description: Anger metadatavärden för en resurs. Fungerar med en array med metadatauppdateringar för att ange värden i en batch.
seo-description: Anger metadatavärden för en resurs. Fungerar med en array med metadatauppdateringar för att ange värden i en batch.
seo-title: setAssetMetadata
solution: Experience Manager
title: setAssetMetadata
topic: Scene7 Image Production System API
uuid: 17fe8277-a164-4f91-af96-ea43d41bd4f2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# setAssetMetadata{#setassetmetadata}

Anger metadatavärden för en resurs. Fungerar med en array med metadatauppdateringar för att ange värden i en batch.

Syntax

## Auktoriserade användartyper {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läsåtkomst till resursen.

## Parametrar {#section-bcdcff30905e444388811e897b2824bd}

**Indata (setAssetMetadataParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget med den tillgång som du vill uppdatera. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Referensen till resursen. |
| ` *`updateArray`*` | `types:MetadataUpdateArray` | Ja | Uppdateringar i en metadatauppdateringsmatris. |

**Utdata (setAssetMetadataReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-1ab412e7ee1d4d6d8469b0b403598c42}

I det här kodexemplet används en array med metadatauppdateringar för att ställa in metadata för den angivna resursen.

**Begäran**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**Svar**

Ingen.
