---
title: Sidvy
description: Huvudvyn består av katalogbilden. Den kan svepas för att komma till en annan sida eller zoomas.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Sidvy{#page-view}

Huvudvyn består av katalogbilden. Den kan svepas för att komma till en annan sida eller zoomas.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col2"> <p> Huvudvyns bakgrundsfärg i hexadecimalt format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> markör </span> </p> </td> 
   <td colname="col2"> <p>Markör som visas över huvudvyn. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att göra huvudvyn genomskinlig.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

På stationära datorer har komponenten stöd för attributväljaren `cursortype` som kan användas på klassen `.s7pageview` och styr typen av markör baserat på komponentens tillstånd och användaråtgärd. Följande `cursortype`-värden stöds:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Värde </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> standard </span> </p> </td> 
   <td colname="col2"> <p>Visas när bilden inte kan zoomas på grund av en liten bildupplösning, komponentinställningar eller båda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>Visas när bilden kan zoomas in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Visas när bilden har maximal zoomnivå och kan återställas till ursprungligt läge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dra </span> </p> </td> 
   <td colname="col2"> <p>Visas när användaren panorerar bilden som är i zoomläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bild </span> </p> </td> 
   <td colname="col2"> <p>Visas när användaren utför en bildväxling genom vågrät dragning eller snärtning. </p> </td> 
  </tr> 
 </tbody> 
</table>

Den sidavgränsare som visuellt skiljer de vänstra och högra sidorna i kataloguppslaget styrs med följande CSS-klassväljare:

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på sidavgränsaren. Ange <span class="codeph"> 0 </span> px för att dölja avgränsaren helt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Bilden som du vill använda som sidavgränsare. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - Att ha en 40 pixlar bred sidavgränsare med halvgenomskinlig bild.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>När modifieraren `frametransition` är inställd på `turn` eller `auto` (på skrivbordssystem) styrs siddelarens utseende med modifieraren `pageturnstyle` och CSS-klassen `.s7pagedivider` ignoreras.

Det går att konfigurera visningen av anpassade musmarkörer över huvudvisningsområdet. Den här funktionen styrs med de ytterligare attributväljarna som används för CSS-klassen `.s7ecatalogsearchviewer .s7pageview`:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> standard </span> </p> </td> 
   <td colname="col2"> <p> Normalt visas en pil för en bild som inte kan zoomas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p> Visar när en bild kan zoomas in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Visar när en bild har zoomats maximalt och kan återställas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dra </span> </p> </td> 
   <td colname="col2"> <p>Visar när användaren utför dra-åtgärd på inzoomad bild </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bild </span> </p> </td> 
   <td colname="col2"> <p>Visar när användaren byter bild med gest </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ha olika musmarkörer för varje typ av komponentläge.

```
.s7ecatalogsearchviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
