---
description: Följande kommandon för styckeformatering stöds.
seo-description: Följande kommandon för styckeformatering stöds.
seo-title: Styckeformatering
solution: Experience Manager
title: Styckeformatering
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f9255b2-3a74-4c9a-80c5-d85b4627027e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Styckeformatering{#paragraph-formatting}

Följande kommandon för styckeformatering stöds.

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Kommando </p> </th> 
   <th class="entry"> <p>Beskrivning </p> </th> 
   <th class="entry"> <p>Anteckningar </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>Återställ styckeformatering till standard. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>Vänsterjustera text. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>Högerjustera text. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>Centrera text vågrätt. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>Justera text vågrätt. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>Vänsterjustera den sista raden i ett stycke. </p> </td> 
   <td> <p>Standard; <span class="codeph"> textPs= </span> only; ignoreras om <span class="codeph"> \qj inte </span>är aktivt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>Högerjustera den sista raden i ett justerat stycke. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignoreras om <span class="codeph"> \qj inte </span> är aktivt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>Centrera den sista raden i ett justerat stycke. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignoreras om <span class="codeph"> \qj inte </span>är aktivt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>Justera (sträck ut) den sista raden i ett justerat stycke. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignoreras om <span class="codeph"> \qj inte </span>är aktivt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span></span> </td> 
   <td> <p>Indrag för första raden. </p> </td> 
   <td> <p>Virvlar; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span></span> </td> 
   <td> <p>Vänster indrag. </p> </td> 
   <td> <p>Virvlar; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span></span> </td> 
   <td> <p>Höger indrag. </p> </td> 
   <td> <p>Virvlar; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span></span> </td> 
   <td> <p>Avståndet mellan raderna. </p> </td> 
   <td> <p>0 (standard) för automatiskt radavstånd; positiva värden som endast använder värden om de är större än standardavståndet, negativt värde för att framtvinga mellanrum. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span></span> </td> 
   <td> <p>Flera flaggor för radavstånd. </p> </td> 
   <td> <p>Ange 0 (standard) om <span class="codeph"> \sl </span> är i twip, till 1 om <span class="codeph"> \sl </span> är i multipler av standardavståndet. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span></span> </td> 
   <td> <p>Extra avstånd före stycke. </p> </td> 
   <td> <p>Virvlar; <span class="codeph"> text= </span>används <span class="codeph"> \sb </span> på det första stycket i textrutan, <span class="codeph"> textPs= </span> gör det inte. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span></span> </td> 
   <td> <p>Extra blanksteg efter stycke. </p> </td> 
   <td> <p>Virvlar; <span class="codeph"> text= </span> används <span class="codeph"> \sa </span> på det sista stycket i textrutan, <span class="codeph"> textPs= </span> gör det inte. </p> </td> 
  </tr> 
 </tbody> 
</table>

