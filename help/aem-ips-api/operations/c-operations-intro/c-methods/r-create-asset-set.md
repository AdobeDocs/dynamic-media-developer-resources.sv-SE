---
description: Skapar en generisk resursuppsättning med en råuppsättningsdefinitionssträng som ska publiceras på en Image Server.
seo-description: Skapar en generisk resursuppsättning med en råuppsättningsdefinitionssträng som ska publiceras på en Image Server.
seo-title: createAssetSet
solution: Experience Manager
title: createAssetSet
topic: Scene7 Image Production System API
uuid: 1e86bd37-511c-4c12-abfd-075053b86f78
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# createAssetSet{#createassetset}

Skapar en generisk resursuppsättning med en råuppsättningsdefinitionssträng som ska publiceras på en Image Server.

Syntax

## Auktoriserade användartyper {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-3580b586296e42a5b21426085b1bb72d}

**Indata (createAssetSet)**

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Obligatoriskt </th> 
   <th colname="col4" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handtaget till företaget som ska innehålla resursuppsättningen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Referensen till mappen där den nya resursuppsättningen ska skapas. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> namn </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Resursnamn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> En unik identifierare som skapats av klienten för resursuppsättningstypen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng </span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Parametrarna i uppsättningsdefinitionssträngen. <p>Dessa måste matcha det format som anges av målvisningsprogrammet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng </span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Hantera den resurs som fungerar som miniatyrbild för den nya bilduppsättningen. Om inget anges försöker IPS använda den första bildresursen som uppsättningen refererar till. </td> 
  </tr> 
 </tbody> 
</table>

**Ersättningsfunktioner för setDefinition**

Du kan ange ersättningsfunktioner på raden som löses vid katalogsökning eller publicering. Ersättningssträngar har formatet `${<substitution_func>}`. Tillgängliga funktioner räknas upp nedan.

>[!NOTE]
>
>Handtagslitteralerna i parameterlistor måste omges av hakparenteser `([])`. All text som ligger utanför en ersättningssträng kopieras ordagrant till utdatasträngen under upplösningen.

| **Ersättningsfunktion** | **Returnerar** |
|---|---|
| `getFilePath([asset_handle>])` | Resursens huvudfilsökväg. |
| `getCatalogId([<asset_handle>])` | Resursens katalog-ID. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Metadatavärden för resursen. |
| `getThumbCatalogId([<asset_handle>])` | Resursens katalog-ID (endast för bildbaserade resurser).Den associerade tumresursens katalog-ID (för andra resurser). Om en associerad tumresurs inte är tillgänglig returnerar funktionen en tom sträng. |

**Exempel på Media setDefinition String**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

Vid katalogsökning eller publiceringstid tolkas detta som en sträng som liknar följande:

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Utdata (createAssetSet)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Ja | Referensen till resursuppsättningen. |

## Exempel {#section-fed53089de824d67ab96cd9103d384b4}

**Begäran**

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**Svar**

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```

