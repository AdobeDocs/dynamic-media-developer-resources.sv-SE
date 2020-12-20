---
description: Uppdaterar uppsättningsdefinitionen för en befintlig resursuppsättning.
seo-description: Uppdaterar uppsättningsdefinitionen för en befintlig resursuppsättning.
seo-title: setAssetSetDefinition
solution: Experience Manager
title: setAssetSetDefinition
topic: Scene7 Image Production System API
uuid: 2a2dce5d-7a01-49af-ac8b-33ae0b234ecc
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# setAssetSetDefinition{#setassetsetdefinition}

Uppdaterar uppsättningsdefinitionen för en befintlig resursuppsättning.

Syntax

## Auktoriserade användartyper {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**Indata (setAssetDefinitionParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget med tillgångsuppsättningen. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Resurshandtag |
| ` *`setDefinition`*` | `xsd:string` | Ja | Definitionssträng. Se nedan. |

**Utdata (setAssetSetDefinitionReturn)**

IPS API returnerar inget svar för den här åtgärden.

## setDefinition-parameter: Om {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**setDefinition-funktioner**

Ange `setDefinition`-ersättningsfunktioner online. De löses under en katalogsökning eller vid publicering. Ersättningssträngar har formatet `${<substitution_func>}` och inkluderar följande:

>[!NOTE]
>
>Referenshandböcker i parameterlistorna måste omges av hakparenteser `([])`. Texten utanför en ersättningssträng kopieras till utdatasträngen under upplösningen.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Ersättningsfunktion </th> 
   <th colname="col2" class="entry"> Returnerar resurserna </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> Primär filsökväg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalog([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> Katalog-ID. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([  <span class="varname"> asset_handle  </span>],[  <span class="varname"> metadata_field_handle  </span>])  </span> </td> 
   <td colname="col2"> Metadatavärde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> Katalog-ID. Gäller för bildbaserade resurser (Bild, Justerad vy, Lagervy). <p>För andra resurser returneras miniatyrresursens katalog-ID (om det finns något). Om ingen tumresurs är associerad med resursen returnerar funktionen en tom sträng. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exempel på setDefinition**

Den här definitionssträngen för medieuppsättningen:

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

Matchar följande vid sökning eller publiceringstid:

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## Exempel {#section-739b42eec3074cafae285ec015a2d088}

**Begäran**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**Svar**

Ingen.
