---
description: Returnerar ZIP-fildata.
solution: Experience Manager
title: getZipEnentries
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---


# getZipEnentries{#getzipentries}

Returnerar ZIP-fildata.

Syntax

## Auktoriserade användartyper {#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-aa3f498fe76d4a5f99c42d64520fadce}

**Indata (getZipEnotesParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget som innehåller ZIP-filen. |
| `*`assetHandle`*` | `xsd:string` | Ja | Hantera zip-filen. |

**Utdata (getZipEnentriesReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`zipArray`*` | `types:ZipEntryArray` | Ja | Array med poster i en ZIP-fil. |

## Exempel {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Det här kodexemplet returnerar information om ZIP-filer, inklusive komprimerad och okomprimerad storlek.

**Begäran**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**Svar**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```

