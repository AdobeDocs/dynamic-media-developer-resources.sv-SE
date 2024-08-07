---
title: Ange indikator
description: Uppsättningsindikatorn är en serie punkter som återges ovanpå färgrutor när ett visningsprogram används på en pekenhet. Med punkter kan användarna navigera genom miniatyrsidor när rullningsknappar inte är tillgängliga.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Ange indikator{#set-indicator}

Uppsättningsindikatorn är en serie punkter som återges ovanpå färgrutor när ett visningsprogram används på en pekenhet. Med punkter kan användarna navigera genom miniatyrsidor när rullningsknappar inte är tillgängliga.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för den angivna indikatorn**

Utseendet på den angivna indikatorbehållaren styrs med följande CSS-klassväljare:

```
.s7zoomviewer .s7setindicator
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

Exempel - Så här skapar du en inställningsindikator med vit bakgrund:

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

Utseendet på en enskild set-indikatorpunkt styrs med CSS-klassväljaren:

`.s7zoomviewer .s7setindicator .s7dot`

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
   <td colname="col1"> <p> <span class="codeph"> marginal-right </span> </p> </td> 
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
 </tbody> 
</table>

>[!NOTE]
>
>Den angivna indikatorpunkten stöder attributväljaren `state` som kan användas för att tillämpa olika skal på olika miniatyrlägen. I synnerhet motsvarar `state="selected"` den aktuella sidan med miniatyrbilder, och `state="unselected"` motsvarar standardpunktläget.

Exempel - Så här skapar du en angiven indikatorpunkt som ska vara 15 x 15 pixlar, med en vågrät marginal på 2 pixlar, en övre marginal på 5 pixlar, en nedre marginal på 12 pixlar, en radie på 12 pixlar, en standardfärg på #D5D3D3 och en aktiv färg på #9393:

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
