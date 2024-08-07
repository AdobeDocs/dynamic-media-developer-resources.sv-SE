---
title: Huvudvisningsområde
description: Huvudvisningsområdet är det område som upptas av zoombilden och färgrutorna. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Huvudvisningsområde{#main-viewer-area}

Huvudvisningsområdet är det område som upptas av zoombilden och färgrutorna. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

När du arbetar i inbäddat läge (när en explicit storlek ges till huvudvisningsområdet) minskar visningsprogrammet automatiskt höjden på huvudområdet med höjden på den färgrutekomponent som arbetar med den enskilda bilden och därför behövs inga färgrutor.

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7zoomviewer
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

Exempel - om du vill konfigurera ett visningsprogram med en vit bakgrund ( `#FFFFFF`) och göra storleken 512 x 288 pixlar.

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
