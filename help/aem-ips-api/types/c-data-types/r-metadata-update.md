---
description: Anger metadatavärden för en specifik resurs som används med setAssetMetadata. Beskriver de ändringar du vill göra i metadata.
seo-description: Anger metadatavärden för en specifik resurs som används med setAssetMetadata. Beskriver de ändringar du vill göra i metadata.
seo-title: MetadataUpdate
solution: Experience Manager
title: MetadataUpdate
topic: Scene7 Image Production System API
uuid: 09d3940b-117d-4d83-8b12-e86520c9da34
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# MetadataUpdate{#metadataupdate}

Anger metadatavärden för en specifik resurs som används med setAssetMetadata. Beskriver de ändringar du vill göra i metadata.

>[!NOTE]
>
>Om fältet med ett värde skickas återställs resursens taggvärde till det angivna taggvärdet.

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
   <td colname="col3"> Fältreferens för metadata. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Värde för metadatauppdatering. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Booleskt metadatavärde (endast för fält av typen Boolean). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Långt metadatavärde (endast för fält av typen int). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dubbel</span> </td> 
   <td colname="col3"> Dubbelt metadatavärde (endast för fält med flyttal). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datummetadatavärde (endast för datumtypsfält). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:StringArray</span> </td> 
   <td colname="col3"> <p>Lägger till i den befintliga taggvärdeslistan för resursen. 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">Enkelvärdesfält lagrar endast det sista värdet. </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">Ett fast ordlistetaggfält returnerar ett fel om värdet inte finns i ordlistan. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:StringArray</span> </td> 
   <td colname="col3">Ersätter den befintliga taggvärdelistan för resursen. 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">Enkelvärdesfält lagrar endast det sista värdet. </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">Ett fast ordlistetaggfält returnerar ett fel om värdet inte finns i ordlistan. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:StringArray</span> </td> 
   <td colname="col3"> Tar bort de angivna värdena från resursens taggvärdeslista, om sådan finns. </td> 
  </tr> 
 </tbody> 
</table>

