---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
topic: Dynamic media
uuid: 6d9541be-d46c-47a7-b75d-879fbba8c7e5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`tal`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Aktivera, begränsa eller inaktivera optimering för enheter där <span class="codeph"> devicePixelRatio</span> är större än <span class="codeph"> 1</span>, det vill säga enheter med högdensitetsvisning som iPhone4 och liknande enheter. Om den är aktiv begränsar komponenten storleken på IS-bildbegäran som om enheten bara hade pixelproportionen <span class="codeph"> 1</span> och på så sätt reducerar bandbredden. </p> <p>Se exemplet nedan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tal</span></span> </p> </td> 
   <td colname="col2"> <p> Om du använder begränsningsinställningen aktiveras endast hög pixeldensitet upp till den angivna gränsen. </p> <p>Se exemplet nedan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-924163cb2f6542499f49894becef7fb5}

Valfritt.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`limit,1500`

## Exempel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

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
   <td colname="col1"> <p><span class="codeph"> alltid</span> </p> </td> 
   <td colname="col2"> <p>Bildskärmens/enhetens pixeldensitet beaktas alltid. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Om skärmens pixeldensitet = 1 är den begärda bilden 1 000 x 1 000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Om skärmpixeldensiteten är 1,5 är den begärda bilden 1 500 x 1 500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Om skärmens pixeldensitet = 2 är den begärda bilden 2 000 x 2 000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> aldrig</span> </p> </td> 
   <td colname="col2"> <p>Den använder alltid en pixeldensitet på 1 och ignorerar enhetens HD-kapacitet. Den begärda bilden är därför alltid 1 000 × 1 000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>En enhets pixeldensitet begärs och hanteras bara om den resulterande bilden är under den angivna gränsen. </p> <p>Gränsnumret gäller antingen för bredden eller höjden. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Om gränsvärdet är 1600 och pixeldensiteten är 1,5 används bilden på 1500 x 1500. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Om gränsvärdet är 1600 och pixeldensiteten är 2 används bilden på 1000 x 1000 eftersom bilden på 2000 x 2000 överskrider gränsvärdet. </p> </li> 
     </ul> </p> <p><b>God praxis</b>: Gränsvärdet måste fungera tillsammans med företagsinställningen för att bilden ska få maximal storlek. Ange därför gränsvärdet som lika med företagets inställning för maximal bildstorlek. </p> </td> 
  </tr> 
 </tbody> 
</table>

