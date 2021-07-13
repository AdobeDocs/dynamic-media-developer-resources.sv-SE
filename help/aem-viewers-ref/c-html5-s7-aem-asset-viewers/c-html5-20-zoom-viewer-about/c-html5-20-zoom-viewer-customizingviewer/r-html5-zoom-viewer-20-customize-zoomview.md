---
description: Huvudvyn består av den zoombara bilden.
solution: Experience Manager
title: Zoomvy
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Zoomvy{#zoom-view}

Huvudvyn består av den zoombara bilden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7zoomviewer .s7zoomview
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
   <td colname="col2"> <p> Bakgrundsfärg i hexadecimalt format för huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> markör  </span> </p> </td> 
   <td colname="col2"> <p>Markören visas över huvudvyn. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att göra huvudvyn genomskinlig.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

På stationära datorer har komponenten stöd för `cursortype`-attributväljare som kan tillämpas på klassen `.s7zoomview`. Den styr typen av markör baserat på komponentens tillstånd och användaråtgärder. Följande `cursortype`-värden stöds:

* `default`

   Visas när bilden inte kan zoomas på grund av en liten bildupplösning, eller komponentinställningar, eller båda.

* `zoomin`

   Visas när bilden kan zoomas in.

* `reset`

   Visas när bilden har maximal zoomnivå och kan återställas till det ursprungliga läget.

* `drag`

   Visas när användaren panorerar bilden som är i zoomläge.

* `slide`

   Visas när användaren byter bild genom att svepa eller snärta vågrätt.
