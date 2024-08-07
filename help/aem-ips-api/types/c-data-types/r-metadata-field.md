---
title: MetadataField
description: Användardefinierade fältdefinitioner för specifika resurser.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 97175076-9078-4bc4-b3ea-73c3ea772f6a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# [!DNL MetadataField]{#metadatafield}

Användardefinierade fältdefinitioner för specifika resurser.

Hämta taggfältsdefinitioner med åtgärderna `getMetadataFields` eller `getAssetMetadataField`.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Fältreferens för metadata. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Namn på metadatafält. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Fälttyp för metadata. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Standardvärde för metadatafältet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isRequired</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Anger obligatorisk status. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isUserDefined</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Avgör om metadatafältet definieras av användaren eller inte. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> isHidden </span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3">Dölj eller visa systemspecifika IPS-metadata. Returnerat från <a href="../../operations/c-operations-intro/c-methods/r-get-metadata-fields.md#reference-170337127801401d9ea54bd4ccf28efe" format="dita" scope="local"> getMetadataFields</a> och <a href="../../operations/c-operations-intro/c-methods/r-get-asset-metadata-fields.md#reference-ea57f8e98d3e443da66114550b0d0a28" format="dita" scope="local"> getAssetMetadataFields</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> <p>En boolesk flagga som anger om metadatafälttypen används (valideras) när värdet ställs in. </p> <p>Om värdet är true genereras ett fel om ett ogiltigt värde anges i <span class="codeph"> setAssetMetadata </span> /<span class="codeph"> batchSetAssetMetadata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Du kan skapa en uppsättning delade angivna värden som markerade taggar kan peka på. </td> 
  </tr> 
 </tbody> 
</table>
