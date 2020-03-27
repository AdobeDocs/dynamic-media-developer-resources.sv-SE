---
description: Vinjetter kan skapas för att innehålla data för nästan 3D-reflektion.
seo-description: Vinjetter kan skapas för att innehålla data för nästan 3D-reflektion.
seo-title: Reflektioner
solution: Experience Manager
title: Reflektioner
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d86f566-0f02-4304-8a6c-08b1a2e9c72e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Reflektioner{#reflections}

Vinjetter kan skapas för att innehålla data för nästan 3D-reflektion.

Om så är fallet används följande materialattribut för att definiera materialets reflekterande ytegenskaper:

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attribut </p> </th> 
   <th class="entry"> <p>Beskrivning </p> </th> 
   <th class="entry"> <p>Standard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> glans=</span></a> </p> </td> 
   <td> <p>Glansighet på ytan </p> </td> 
   <td> <p>Från vinjett </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span></a> </p> </td> 
   <td> <p>Glanvariation (gråskalebild) </p> </td> 
   <td> <p>Ingen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> grov= </span></a> </p> </td> 
   <td> <p>Ytojämnhet </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span></a> </p> </td> 
   <td> <p>Materialtyp </p> </td> 
   <td> <p>0 (okänd) </p> </td> 
  </tr> 
 </tbody> 
</table>

Renderaren justerar omfånget för attributet `gloss=` och `rough=` enligt `type=`. Vissa typer av material, t.ex. tyger, reflekterar i allmänhet mindre än materialtyper som sten eller metall, och samma mängd glans som anges för den ena ger en annan reflektionseffekt än den andra. `gloss=`och grovhet har ett tämligen brett färgomfång om `type=` inte anges eller är inställt på 0.

`glossmap=` kan användas för att kontrollera glansigheten i ett material pixelvis.
