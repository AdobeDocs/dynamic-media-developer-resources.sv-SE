---
description: Hämtar tillgångarna och antalet tillgångar som är associerade med ett visst företag.
seo-description: Hämtar tillgångarna och antalet tillgångar som är associerade med ett visst företag.
seo-title: getAssetCount
solution: Experience Manager
title: getAssetCount
topic: Scene7 Image Production System API
uuid: 92103806-59da-444f-b69c-d045d0ebf42e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# getAssetCount{#getassetcounts}

Hämtar tillgångarna och antalet tillgångar som är associerade med ett visst företag.

Det `countArray` som returneras består av en matris med `assetTypes` (datatypen `xsd:string`), där vart och ett har ett eget räkningsfält (datatypen `xsd:int`), som tillåter representationen av flera resurstyper per element i matrisen.
Syntax

## Auktoriserade användartyper {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**Indata (getAssetCountsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget med resurser som du vill räkna. |

**Utdata (getAssetCountReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`countArray`*` | `types:AssetCountArray` | Nej | En array med resurstyper, var och en med ett eget räkningsfält, som tillåter representationen av flera resurstyper per element i arrayen. |

## Exempel {#section-6052a503eb3843f6adb99e200fdba280}

I det här kodexemplet används företagets referens som ett fält i `getAssetCountsParam` som skickas till IPS Web services-servern för att få fram antalet mediefiler.

**Begäran**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**Svar**

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```

