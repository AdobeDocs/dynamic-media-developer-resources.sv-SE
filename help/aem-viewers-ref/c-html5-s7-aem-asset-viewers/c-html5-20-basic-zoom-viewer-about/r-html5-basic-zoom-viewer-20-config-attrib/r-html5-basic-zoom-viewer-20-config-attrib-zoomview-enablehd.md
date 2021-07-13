---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Zoom
role: Developer,User
exl-id: 321ca7e2-e3f9-4b0e-8bde-41d8478e1a0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`tal`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Aktivera, begränsa eller inaktivera optimering för enheter där <span class="codeph"> devicePixelRatio</span> är större än <span class="codeph"> 1</span>, det vill säga enheter med högdensitetsvisning som iPhone4 och liknande enheter. Om den är aktiv begränsar komponenten storleken på IS-bildbegäran som om enheten bara hade ett pixelförhållande på <span class="codeph"> 1</span> och på så sätt minskar bandbredden. </p> <p>Se exemplet nedan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tal</span> </span> </p> </td> 
   <td colname="col2"> <p> Om du använder begränsningsinställningen aktiveras endast hög pixeldensitet upp till den angivna gränsen. </p> <p>Se exemplet nedan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-50bcd15223174bb79ce08b31ea03d682}

Valfritt.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## Exempel {#section-96e69b70365f461dae4399e49044ea2f}

Nedan följer de förväntade resultaten när du använder det här konfigurationsattributet med visningsprogrammet och visningsprogrammets storlek är 1 000 x 1 000:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Om den angivna variabeln är lika med </p> </th> 
   <th colname="col2" class="entry"> <p>Resultat </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alltid</span> </p> </td> 
   <td colname="col2"> <p>Bildskärmens/enhetens pixeldensitet beaktas alltid. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Om skärmens pixeldensitet = 1 är den begärda bilden 1 000 x 1 000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Om skärmpixeldensiteten är 1,5 är den begärda bilden 1 500 x 1 500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Om skärmens pixeldensitet = 2 är den begärda bilden 2 000 x 2 000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aldrig</span> </p> </td> 
   <td colname="col2"> <p>Den använder alltid en pixeldensitet på 1 och ignorerar enhetens HD-kapacitet. Den begärda bilden är därför alltid 1 000 × 1 000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>En enhets pixeldensitet begärs och hanteras bara om den resulterande bilden är under den angivna gränsen. </p> <p>Gränsnumret gäller antingen för bredden eller höjden. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Om gränsvärdet är 1600 och pixeldensiteten är 1,5 används bilden på 1500 x 1500. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Om gränsvärdet är 1600 och pixeldensiteten är 2 används bilden på 1000 x 1000 eftersom bilden på 2000 x 2000 överskrider gränsvärdet. </p> </li> 
     </ul> </p> <p> <b>God praxis</b>: Gränsvärdet måste fungera tillsammans med företagsinställningen för att bilden ska få maximal storlek. Ange därför gränsvärdet som lika med företagets inställning för maximal bildstorlek. </p> </td> 
  </tr> 
 </tbody> 
</table>
