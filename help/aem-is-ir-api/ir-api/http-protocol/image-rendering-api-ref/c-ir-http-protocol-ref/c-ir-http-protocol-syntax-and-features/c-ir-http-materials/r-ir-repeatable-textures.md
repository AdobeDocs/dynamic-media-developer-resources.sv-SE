---
title: Upprepningsbara texturer
description: Upprepningsbara texturer är bland annat inre och yttre material, t.ex. vävnader (både kläder och möbelklädsel), golvbeläggning från vägg till vägg, tapeter, motverkande material, texturer av trä, takbeklädnad och sidomaterial samt all annan allmän textur.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Upprepningsbara texturer{#repeatable-textures}

Upprepningsbara texturer är bland annat inre och yttre material, t.ex. vävnader (både kläder och möbelklädsel), golvbeläggning från vägg till vägg, tapeter, motverkande material, texturer av trä, takbeklädnad och sidomaterial samt all annan allmän textur.

Upprepningsbara texturer kan användas på plana, flödeslinjer, skisser, plan, vägg och kabinettobjekt. När objektet används på ett objekt som inte är texturerbart målas det med `color=` (eller `bgc=` om `color=` inte anges).

Ett material betraktas som en textur om det innehåller ett `src=`-attribut som anger en bild och om det förekommer i en annan MSS än en dekal- eller väggkant.

Vid återgivning justeras texturen efter objektet genom att matcha `anchor=`-punkten i texturmaterialet med objektets texturorigo (som skapad i vinjetteringen).

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
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
   <td colname="col2"> <p>Upprepningsbar texturbild; krävs </p> </td> 
   <td colname="col3"> <p>Ingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Texturupplösning </p> </td> 
   <td colname="col3"> <span class="codeph">-attribut::Upplösning </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span> </a> </p> </td> 
   <td colname="col2"> <p>Texturjusteringspunkt </p> </td> 
   <td colname="col3"> <p>Övre vänstra hörnet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>Repeteringsläge </p> </td> 
   <td colname="col3"> <p>0 (rak upprepning). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Skärpa </p> </td> 
   <td colname="col3"> <p>0 (ingen skärpa). </p> </td> 
  </tr> 
 </tbody> 
</table>

Utöver dessa grundläggande attribut stöder upprepningsbara texturer följande specialattribut för avancerade program:

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
   <th colname="col3" class="entry"> <p>Standard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grout= </span> </a> </p> </td> 
   <td colname="col2"> <p>Grovfärg och tjocklek, användbart för keramiska/stenplattor </p> </td> 
   <td colname="col3"> <p>Grovt finns redan i bilden </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align= </span> </a> </p> </td> 
   <td colname="col2"> <p>Justeringsläge (mellan objekt); används för möbelklädda program </p> </td> 
   <td colname="col3"> <p>Centrerad </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>Texturrotationsvinkel; stöds inte av väggobjekt </p> </td> 
   <td colname="col3"> <p>0 (ingen rotation) </p> </td> 
  </tr> 
 </tbody> 
</table>
