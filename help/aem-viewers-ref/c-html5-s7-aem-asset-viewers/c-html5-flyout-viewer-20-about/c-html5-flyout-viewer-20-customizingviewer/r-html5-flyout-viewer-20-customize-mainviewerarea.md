---
description: Huvudvisningsområdet är det område som upptas av den utfällbara vyn och färgrutorna.
seo-description: Huvudvisningsområdet är det område som upptas av den utfällbara vyn och färgrutorna.
seo-title: Huvudvisningsområde
solution: Experience Manager
title: Huvudvisningsområde
topic: Dynamic media
uuid: bc0beeaf-3e7d-4ede-9a7d-04afb1724e44
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Huvudvisningsområde{#main-viewer-area}

Huvudvisningsområdet är det område som upptas av den utfällbara vyn och färgrutorna.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7flyoutviewer
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredden på visningsprogrammet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Visningsprogrammets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärg i hexadecimalt format. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in ett utfällbart visningsprogram med vit bakgrund ( `#FFFFFF`) och göra dess storlek 260 x 500 pixlar.

```
.s7flyoutviewer { 
 background-color: #FFFFFF; 
 width: 260px; 
 height: 500px;  
}
```

