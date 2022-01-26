---
title: Ange indikator
description: Uppsättningsindikatorn är en serie punkter som återges ovanpå huvudfärgrutorna när ett visningsprogram används på en pekenhet. Med punkter kan användarna navigera genom miniatyrsidor när rullningsknappar inte är tillgängliga.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 53ee058a-cb8c-4b1f-bb9b-caaecc12c947
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Ange indikator{#set-indicator}

Uppsättningsindikatorn är en serie punkter som återges ovanpå huvudfärgrutorna när ett visningsprogram används på en pekenhet. Med punkter kan användarna navigera genom miniatyrsidor när rullningsknappar inte är tillgängliga.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för den angivna indikatorn**

Utseendet på den angivna indikatorbehållaren styrs med följande CSS-klassväljare:

```
.s7mixedmediaviewer .s7setindicator
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
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

Utseendet på en enskild set-indikatorpunkt styrs med CSS-klassväljaren:

`.s7mixedmediaviewer .s7setindicator .s7dot`

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
 </tbody> 
</table>

>[!NOTE]
>
>Ange indikatorpunkt för `state` attributväljare, som kan användas för att tillämpa olika skal på olika miniatyrlägen. I synnerhet `state="selected"` motsvarar den aktuella sidan med miniatyrbilder, `state="unselected"` motsvarar standardpunktläget.

Exempel - Så här skapar du en angiven indikatorpunkt som är 15 x 15 pixlar, med en vågrät marginal på två pixlar, en övre marginal på fem pixlar, en nedre marginal på en pixel, en radie på 12 pixlar, standardfärgen #D5D3D3 och den aktiva färgen #9393:

```
.s7mixedmediaviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7mixedmediaviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
