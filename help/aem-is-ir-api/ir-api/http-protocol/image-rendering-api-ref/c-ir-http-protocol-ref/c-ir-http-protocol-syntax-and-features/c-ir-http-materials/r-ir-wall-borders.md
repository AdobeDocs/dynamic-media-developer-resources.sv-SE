---
description: Ett material betraktas som en väggkant när det anges i en väggkant (MSS) (introducerades med sub=3.5).
seo-description: Ett material betraktas som en väggkant när det anges i en väggkant (MSS) (introducerades med sub=3.5).
seo-title: Väggkanter
solution: Experience Manager
title: Väggkanter
topic: Scene7 Image Serving - Image Rendering API
uuid: 40acd667-5e8b-4425-b44a-0681e608d189
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Väggkanter{#wall-borders}

Ett material betraktas som en väggkant när det anges i en väggkant (MSS) (introducerades med sub=3.5).

Texturbilder för väggkanter kan innehålla en alfakanal som definierar kantens form. Väggkanter kan bara användas på väggobjekt.

<table id="table_906C5CC4CADF4024AA0E29544AF48080"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
   <th colname="col3" class="entry"> <p>Standard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>Upprepningsbar texturbild; obligatoriskt </p> </td> 
   <td colname="col3"> <p>Ingen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>Texturupplösning </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span></a> </p> </td> 
   <td colname="col2"> <p>Vågrät texturjustering (y-värdet ignoreras) </p> </td> 
   <td colname="col3"> <p>0 (vänster bildkant) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span></a> </p> </td> 
   <td colname="col2"> <p>Skärpa </p> </td> 
   <td colname="col3"> <p>0 (ingen skärpa) </p> </td> 
  </tr> 
 </tbody> 
</table>

