---
description: Huvudvisningsområdet är det område som upptas av zoombilden och färgrutorna. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.
seo-description: Huvudvisningsområdet är det område som upptas av zoombilden och färgrutorna. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.
seo-title: Huvudvisningsområde
solution: Experience Manager
title: Huvudvisningsområde
topic: Dynamic media
uuid: 689116cb-bbb9-4e26-9c16-9229330c4034
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Huvudvisningsprogramområde{#main-viewer-area}

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
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Visningsprogrammets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärg i hexadecimalt format. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in ett visningsprogram med en vit bakgrund ( `#FFFFFF`) och göra storleken 512 x 288 pixlar.

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

