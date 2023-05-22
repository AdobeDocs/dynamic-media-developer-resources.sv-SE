---
title: Ange indikator
description: Uppsättningsindikatorn är en serie punkter som återges längst ned i visningsprogrammet. Här visas den aktuella positionen i uppsättningen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Ange indikator{#set-indicator}

Uppsättningsindikatorn är en serie punkter som återges längst ned i visningsprogrammet. Här visas den aktuella positionen i uppsättningen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för den angivna indikatorn**

Utseendet på den angivna indikatorbehållaren styrs med följande CSS-klassväljare:

```
.s7carouselviewer .s7setindicator
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärgen i hexadecimalt format för uppsättningsindikatorn. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Set-indikatorn har stöd för lägesattributväljaren, som du kan använda för att använda olika format för prickade och numeriska operationslägen. I synnerhet `mode="numeric"` motsvarar det numeriska driftsläget, `mode="dotted"` motsvarar standardpunktläget.

Anta till exempel att du vill ställa in en uppsättningsindikator med vit bakgrund:

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

Utseendet på en enskild indikatorpunkt för uppsättning styrs med CSS-klassväljaren. Det gäller för objekt både i prickat och numeriskt läge.

`.s7carouselviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredden på den angivna indikatorpunkten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på den angivna indikatorpunkten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-vänster </span> </p> </td> 
   <td colname="col2"> <p>Vänstermarginal i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-top </span> </p> </td> 
   <td colname="col2"> <p>Övre marginal i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-höger </span> </p> </td> 
   <td colname="col2"> <p>Högermarginal i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-bottom </span> </p> </td> 
   <td colname="col2"> <p>Undre marginal i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Kantradie i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärg i hexadecimalt format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittets namn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Teckenfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> lodrät justering </span> </p> </td> 
   <td colname="col2"> <p>Banderollindexets lodräta justering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Texthöjd för banderollindexet. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ange att indikatorobjekt har stöd för `state` attributväljare, som kan användas för att tillämpa olika skal på olika miniatyrlägen. I synnerhet `state="selected"` motsvarar det aktuella elementet i uppsättningen, `state="unselected"` motsvarar standardobjektläget.

Anta till exempel att du vill ställa in en angiven indikator i prickat läge för stationära datorer. Du vill att den ska placeras 20 pixlar från visningsprogrammets nederkant. Och du vill att omarkerade punkter ska vara svarta med 50 % genomskinlighet, 15 x 15 pixlar med sju pixlar rundade hörn. Markerade punkter är svarta med 90 % genomskinlighet, 18 x 18 pixlar med nio pixlar rundade hörn. Avståndet mellan punkter är fem pixlar.

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```
