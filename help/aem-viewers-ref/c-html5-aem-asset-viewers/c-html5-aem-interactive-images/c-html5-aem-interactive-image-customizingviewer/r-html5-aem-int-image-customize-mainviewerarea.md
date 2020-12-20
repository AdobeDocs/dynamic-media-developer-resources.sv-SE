---
description: Huvudvisningsområdet är det område som upptas av zoombilden. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.
seo-description: Huvudvisningsområdet är det område som upptas av zoombilden. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.
seo-title: Huvudvisningsområde
solution: Experience Manager
title: Huvudvisningsområde
topic: Dynamic media
uuid: 666328fe-1819-43a6-a2c2-ba63ac798700
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# Huvudvisningsprogramområde{#main-viewer-area}

Huvudvisningsområdet är det område som upptas av zoombilden. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7interactiveimage
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
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Visningsprogrammets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärg i hexadecimalt format. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in ett visningsprogram med en vit bakgrund ( `#FFFFFF`) och göra dess storlek 1 174 x 500 pixlar.

```
.s7interactiveimage { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```

