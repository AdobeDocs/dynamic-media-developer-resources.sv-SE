---
description: Fönsterbeläggning omfattar både mjuka fönsterbeläggningar (drapes, valances, café curtains) och hårda fönsterbeläggningar (shades and blinds).
seo-description: Fönsterbeläggning omfattar både mjuka fönsterbeläggningar (drapes, valances, café curtains) och hårda fönsterbeläggningar (shades and blinds).
seo-title: Fönsteromslag
solution: Experience Manager
title: Fönsteromslag
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d74466a-b7c3-43b0-9b0b-f8bb809e2773
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# Fönsteromslag{#window-coverings}

Fönsterbeläggning omfattar både mjuka fönsterbeläggningar (drapes, valances, café curtains) och hårda fönsterbeläggningar (shades and blinds).

Fönsteromfattande material anger ett *fönster som omfattar formatfilen* ( [!DNL .vnw] filtillägg), en särskild datafil som liknar en vinjettering, som innehåller masker, belysning, layout och texturdata som definierar fönsteromslaget.

[!DNL vnw] -filer innehåller inte färg och struktur (struktur) för fönsteröverdraget. Denna information specificeras separat, på liknande sätt som repeterbara texturer.

Det går bara att använda fönsteromslagsmaterial på fönsterobjekt som är överlappande objekt.

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
   <th colname="col3" class="entry"> <p>Standard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Fönsteromfattande formatfil. krävs. </p> </td> 
   <td colname="col3"> <p>Ingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Strukturbildfil (andra värdet för <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Ingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Texturupplösning. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Upprepa läge. </p> </td> 
   <td colname="col3"> <p>0 (rak upprepning) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Enfärgad (eller färglägger textur). </p> </td> 
   <td colname="col3"> <p>128 (neutralt grått) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Skärpa. </p> </td> 
   <td colname="col3"> <p>0 (ingen skärpa) </p> </td> 
  </tr> 
 </tbody> 
</table>

