---
description: Hämtar de ursprungliga filsökvägarna för ett företags resurser.
seo-description: Hämtar de ursprungliga filsökvägarna för ett företags resurser.
seo-title: getOriginalFilePaths
solution: Experience Manager
title: getOriginalFilePaths
topic: Scene7 Image Production System API
uuid: c4acf288-1a57-4295-806b-348f15a089cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getOriginalFilePaths{#getoriginalfilepaths}

Hämtar de ursprungliga filsökvägarna för ett företags resurser.

Syntax

## Auktoriserade användartyper {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Kräver läsåtkomst till resursen.

## Parametrar {#section-a6b394daba6e49a8882cf3051035d9d1}

**Indata (getOriginalFilePathsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Ja | En array med handtag till resurser vars ursprungliga filsökväg du vill hämta. |

**Utdata (getOriginalFilePathsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`originalFileArray`*` | `types:StringArray` | Ja | Arrayen med strängar som representerar de ursprungliga filsökvägarna. |

## Exempel {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Detta kodexempel returnerar filsökvägarna för resurser som anges med unika resurshandtag i en resurshandtag.

**Begäran**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**Svar**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```

