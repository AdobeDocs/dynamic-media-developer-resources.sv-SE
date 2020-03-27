---
description: Kontrollerar om det finns IPS ID-konflikter genom att jämföra resursnamn med alla namn i ett företags namnområde Bildserver/Bildåtergivningskatalog.
seo-description: Kontrollerar om det finns IPS ID-konflikter genom att jämföra resursnamn med alla namn i ett företags namnområde Bildserver/Bildåtergivningskatalog.
seo-title: checkAssetNames
solution: Experience Manager
title: checkAssetNames
topic: Scene7 Image Production System API
uuid: 91d073a8-7648-429b-aa5c-c7d595550299
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# checkAssetNames{#checkassetnames}

Kontrollerar om det finns IPS ID-konflikter genom att jämföra resursnamn med alla namn i ett företags namnområde Bildserver/Bildåtergivningskatalog.

Syntax

## Auktoriserade användartyper {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parametrar {#section-9c75b00f2072453abea0bdefc6ad7c99}

**Indata (checkAssetNamesParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Nej | Referensen till företaget som innehåller användaren. |
| ` *`assetNamesArray`*` | `types:StringArray` | Ja | En array med resursnamn som ska kontrolleras. |

**Utdata (checkAssetNamesReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`inUseNameArray`*` | `types:StringArray` | Ja | En array med resursnamn som används. |

## Exempel {#section-bc5d120d74614a63a425ca3acc337219}

Den här exempelkoden begär de resursnamn som används för ett angivet företag. Svaret returnerar en array med resursnamn som används.

**Begäran**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**Svar**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```

