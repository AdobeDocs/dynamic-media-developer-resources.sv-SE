---
description: Sök efter resurser baserat på dina angivna villkor.
seo-description: Sök efter resurser baserat på dina angivna villkor.
seo-title: searchAssets
solution: Experience Manager
title: searchAssets
topic: Scene7 Image Production System API
uuid: 125e9e0d-1856-4e80-9778-ca93cd04b766
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---


# searchAssets{#searchassets}

Sök efter resurser baserat på dina angivna villkor.

Syntax

## searchAssets: Om {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` är den primära metoden för att hämta IPS-resurser. Den här metoden används för olika syften, till exempel för att bläddra i mapphierarkin eller för att hitta en specifik resurs efter namn.

**Svarsstorlek**

`searchAssets` returnerar upp till 1 000 resurser i ett enda samtal. Om du vill returnera upp till 10 000 resurser per anrop begränsar du svarsdata till en delmängd av `totalRows`fälten, `name`, `handle``type`och `subType` . Om du vill returnera större uppsättningar ställer du in sidindelning med `resultPage` parametern.

**Begränsa resultatfilens storlek med responseFieldArray eller excludeFieldArray**

Begränsa storleken på datauppsättningen med parametrarna `responseFieldArray` eller `excludFieldArray` . De här parametrarna minskar minnesanvändningen och bandbredden och kan förbättra svarstiderna på servern.

## Auktoriserade användartyper {#section-9c4bc41bb8b4493982197eb13c7cdc55}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läsåtkomst för att kunna returnera resurser.

## Parametrar {#section-49aabc0600764f55a8b7017d86ded44f}

**Indata (searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Obligatoriskt? </th> 
   <th colname="col4" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handtaget till företaget med de resurser som du vill söka efter. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Gör att administratörer kan arbeta som en annan användare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Gör att administratörer kan arbeta som en del av en annan grupp. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mapp</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Rotsökvägen för att söka efter resurser. Om det utelämnas används företagets rotmapp. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4">Ange som <span class="codeph"> true</span> om du vill söka efter undermappar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Välj publiceringstillstånd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4">Val av papperskorgsläge. Standardvärdet är <span class="codeph"> NotInTrash</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Val av sökmatchningslägen för kombination av resultat av <span class="codeph"> keywordArray</span>, </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span>och <span class="codeph"> metadataConditionArray</span>. Standard är <span class="codeph"> MatchAll</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:StringArray</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p> <p>Obs!  Inaktuell parameter. Det rekommenderas att du inte använder den. </p> </p> <p>En strängarray med nyckelord som ska matchas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Val av sökmatchningslägen för kombination av <span class="codeph"> systemFieldCondition</span> -matchningar. Standard är <span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> typer:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Arrayen med systemfältvillkor. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4">Sök efter strängkonstanter för Matcha lägen. Standardvärdet är <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:TagConditionArray</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>En array med sökpredikat för taggfält. </p> <p>Predikaten kombineras enligt inställningen <span class="codeph"> tagMatchMode</span> och kombineras sedan med andra termer i <span class="codeph"> keywordArray</span>, <span class="codeph"> systemFieldConditionArray</span>och <span class="codeph"> metadataConditionArray</span> enligt inställningen <span class="codeph"> conditionMatchMode</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4">Sök i Matcha lägen för att kombinera <span class="codeph"> metadataVillkorskoder</span> . Standard är <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> typer:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Arrayen med sökvillkor för metadatafält. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:StringArray</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Array med resurstyper som ska ingå i sökningen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:StringArray</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> En array med resurstyper som ska uteslutas från sökningen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:StringArray</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> En lista med undertypsnamn att filtrera mot. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4">Om <span class="codeph"> true</span> och <span class="codeph"> assetSubTypeArray</span> inte är tom returneras bara resurser vars undertyper finns i <span class="codeph"> assetSubTypeArray</span> . Om värdet är <span class="codeph"> false</span> (standard) returneras resurser utan definierad undertyp. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Om värdet är true exkluderas de produktresurser som genereras vid inmatning av en primär resurs, t.ex. bilder på bortskurna PDF-sidor, från sökresultaten. Standardvärdet är false. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> typer:ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Matris med villkor för generering av produktresurser som ska uteslutas från sökresultatet. Om den här parametern finns åsidosätter den inställningen excludeByproducts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sting</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Hantering av ett projekt som innehåller de resurser som ska sökas igenom. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Maximalt antal resultat som ska returneras. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4">Anger vilken resultatsida som ska returneras baserat på <span class="codeph"> recordsPerPage</span> -sidstorleken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Val av resurssorteringsfält. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Val av sorteringsriktning. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:StringArray</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Innehåller en lista med fält och underfält som ska inkluderas i svaret. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:StringArray</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Innehåller en lista med fält och underfält som ska uteslutas från svaret. </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (searchAssetsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`totalRows`*` | `xsd:int` | Nej | Antal rader som en sökning returnerar när poster per sida inte är begränsade. |
| ` *`assetArray`*` | `types:AssetArray` | Nej | Resurser som sökningen returnerar. |

## Exempel {#section-725484cc09b54772a838ad2cc930b94b}

Det här kodexemplet söker efter bildresurser som tillhör ett visst företag. Svaret kortas av för att vara kortfattat.

**Begäran**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**Svar**

```java
<searchAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <totalRows>210</totalRows>
   <assetArray>
      <items>
         <assetHandle>24265|1|17061</assetHandle>
         <type>Image</type>
         <name>Autumn Leaves</name>
         ...
      </items>
    </assetArray>
</searchAssetsReturn>
```

