---
description: Lägger till en sökterm som ska användas med searchAssets.
solution: Experience Manager
title: MetadataCondition
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 9226fb81-b3ff-41e4-a3cd-d5a40f359be6
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# MetadataCondition{#metadatacondition}

Lägger till en sökterm som ska användas med searchAssets.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Fälthandtag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Val av operatorer för strängjämförelse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Värde att testa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Booleskt jämförelsevärde (endast för fält av typen Boolean). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Långt jämförelsevärde (endast för fält av typen int). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minLong</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Minsta långa värde i intervalljämförelse (endast för fält av typen int). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxLong</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Maxvärde för långt värde i intervalljämförelse (endast för fält av typen int). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dubbel</span> </td> 
   <td colname="col3"> Dubbelt jämförelsevärde (endast för fält med flyttal). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minDouble</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dubbel</span> </td> 
   <td colname="col3"> Minsta dubbelvärde i intervalljämförelse (endast för fält med flyttal). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxDouble</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dubbel</span> </td> 
   <td colname="col3"> Högsta dubbla värde i intervalljämförelse (endast för flyttalsfält). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datumjämförelsevärde (endast för datumtypsfält). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Minsta datumvärde i intervalljämförelse (endast för datumtypsfält). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Högsta datumvärde i intervalljämförelse (endast för datumtypsfält). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> caseSensitive</span> </span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p> Fastställer skiftlägeskänslighet för metadataservern. Används i anropet <span class="codeph"> searchAssetsByMetadata</span>. </p> <p>Se <a href="../../operations/c-operations-intro/c-methods/r-search-assets-by-metadata.md#reference-609ec73944a34ce49b152389fbb40414" format="dita" scope="local"> searchAssetsByMetadata</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>
