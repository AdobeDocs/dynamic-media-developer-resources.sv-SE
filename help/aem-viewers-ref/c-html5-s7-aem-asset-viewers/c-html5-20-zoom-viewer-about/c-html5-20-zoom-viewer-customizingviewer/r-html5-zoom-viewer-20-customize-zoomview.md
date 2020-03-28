---
description: Huvudvyn består av den zoombara bilden.
seo-description: Huvudvyn består av den zoombara bilden.
seo-title: Zoomvy
solution: Experience Manager
title: Zoomvy
topic: Dynamic media
uuid: 34cb6c80-77eb-42b0-91dd-ae0369ea2881
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärg i hexadecimalt format för huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> markör </span> </p> </td> 
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

På datorer har komponenten stöd för `cursortype` attributväljare som kan användas på `.s7zoomview` klassen. Den styr typen av markör baserat på komponentens tillstånd och användaråtgärder. Följande `cursortype` värden stöds:

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

