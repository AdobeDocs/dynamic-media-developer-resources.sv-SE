---
description: Huvudvisningsområdet är det område som upptas av zoombilden. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.
seo-description: Huvudvisningsområdet är det område som upptas av zoombilden. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.
seo-title: Huvudvisningsområde
solution: Experience Manager
title: Huvudvisningsområde
topic: Dynamic media
uuid: f37b8d25-4bd6-481e-88e7-98192186b177
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Huvudvisningsprogramområde{#main-viewer-area}

Huvudvisningsområdet är det område som upptas av zoombilden. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7basiczoomviewer
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

Exempel - om du vill ställa in ett visningsprogram med vit bakgrund ( `#FFFFFF`) och göra dess storlek 512 x 288 pixlar.

```
.s7basiczoomviewer{ 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

