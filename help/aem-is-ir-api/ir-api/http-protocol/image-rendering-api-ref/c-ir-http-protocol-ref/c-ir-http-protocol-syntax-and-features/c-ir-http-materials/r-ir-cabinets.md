---
title: Skåp
description: Kabinettmaterial anger en kabinettformatfil (.vnc-filtillägg), en särskild datafil som innehåller fotografiska representationer av skåp tillsammans med parameterlayoutdefinitioner och annan information som krävs för återgivning av skåftets framsidor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Skåp{#cabinets}

Kabinettmaterial anger en kabinettformatfil (.vnc-filtillägg), en särskild datafil som innehåller fotografiska representationer av skåp tillsammans med parameterlayoutdefinitioner och annan information som krävs för återgivning av skåftets framsidor.

[!DNL vnc] filerna kan innehålla en repeterbar kornstextur, eller så kan texturen ges externt via ett andra argument till `src=`. Vissa [!DNL vnc] filer kan användas för att färgsätta eller texturera valda områden i skåpsrutor (används vanligtvis för att laminera skåpsstilar).

Kabinettmaterial kan bara användas på kabinettobjekt.

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
   <th colname="col3" class="entry"> <p>Standard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Kabinettformatfil; krävs. </p> </td> 
   <td colname="col3"> <p>Ingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Valfri texturbildfil (andra värdet för <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Ingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Valfri texturupplösning. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span> </a> </p> </td> 
   <td colname="col2"> <p>Färgar skåp och/eller textur. </p> </td> 
   <td colname="col3"> <p>Ingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Skärpa. </p> </td> 
   <td colname="col3"> <p>0 (ingen skärpa) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> flags= </span> </a> </p> </td> 
   <td colname="col2"> <p>Särskilda återgivningsflaggor. </p> </td> 
   <td colname="col3"> <p>0 (inga flaggor) </p> </td> 
  </tr> 
 </tbody> 
</table>
