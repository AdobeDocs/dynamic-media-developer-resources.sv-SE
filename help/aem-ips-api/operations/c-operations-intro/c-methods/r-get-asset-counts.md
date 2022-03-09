---
description: Hämtar tillgångarna och antalet tillgångar som är associerade med ett visst företag.
solution: Experience Manager
title: getAssetCount
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# getAssetCount{#getassetcounts}

Hämtar tillgångarna och antalet tillgångar som är associerade med ett visst företag.

The `countArray` returnerade består av en array med `assetTypes` (datatyp `xsd:string`), vart och ett med sitt eget räkningsfält (datatyp `xsd:int`), som tillåter representationen av flera resurstyper per element i arrayen.
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
| companyHandle | `xsd:string` | Ja | Handtaget till företaget med resurser som du vill räkna. |

**Utdata (getAssetCountReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| countArray | `types:AssetCountArray` | Nej | En array med resurstyper, var och en med ett eget räkningsfält, som tillåter representationen av flera resurstyper per element i arrayen. |

## Exempel {#section-6052a503eb3843f6adb99e200fdba280}

I det här kodexemplet används företagets referens som ett fält i `getAssetCountsParam` skickas till IPS-webbtjänstservern för att få tillgång till antalet resurser.

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
