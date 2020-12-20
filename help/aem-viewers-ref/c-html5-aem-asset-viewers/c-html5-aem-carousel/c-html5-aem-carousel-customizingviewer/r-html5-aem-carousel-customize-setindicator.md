---
description: Uppsättningsindikatorn är en serie punkter som återges längst ned i visningsprogrammet. Här visas den aktuella positionen i uppsättningen.
seo-description: Uppsättningsindikatorn är en serie punkter som återges längst ned i visningsprogrammet. Här visas den aktuella positionen i uppsättningen.
seo-title: Ange indikator
solution: Experience Manager
title: Ange indikator
topic: Dynamic media
uuid: 3f90a216-654f-44a9-947d-592bd5f342d4
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '338'
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärgen i hexadecimalt format för uppsättningsindikatorn. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Set-indikatorn har stöd för lägesattributväljaren, som du kan använda för att använda olika format för prickade och numeriska operationslägen. `mode="numeric"` motsvarar i synnerhet det numeriska driftsläget; `mode="dotted"` motsvarar standardpunktläget.

Exempel - för att ställa in en inställningsindikator med en vit bakgrund:

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
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höjden på den angivna indikatorpunkten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-vänster  </span> </p> </td> 
   <td colname="col2"> <p>Vänstermarginal i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-top  </span> </p> </td> 
   <td colname="col2"> <p>Övre marginal i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-höger  </span> </p> </td> 
   <td colname="col2"> <p>Högermarginal i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-bottom  </span> </p> </td> 
   <td colname="col2"> <p>Undre marginal i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>Kantradie i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärg i hexadecimalt format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittets namn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg  </span> </p> </td> 
   <td colname="col2"> <p>Teckenfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> lodrät justering  </span> </p> </td> 
   <td colname="col2"> <p>Banderollindexets lodräta justering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p>Texthöjd för banderollindexet. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De angivna indikatorobjekten stöder attributväljaren `state`, som kan användas för att tillämpa olika skal på olika miniatyrlägen. `state="selected"` motsvarar i synnerhet det aktuella elementet i uppsättningen; `state="unselected"` motsvarar standardobjektets tillstånd.

Exempel - för att ställa in en inställningsindikator i prickat läge för datorer som ska placeras 20 pixlar från visningsprogrammets nederkant. Omarkerade punkter är svarta med 50 % genomskinlighet, 15 x 15 pixlar med 7 pixlar rundade hörn. Markerade punkter är svarta med 90 % genomskinlighet, 18 x 18 pixlar med 9 pixlar rundade hörn. Mellanrummet mellan punkter är 5 pixlar.

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

