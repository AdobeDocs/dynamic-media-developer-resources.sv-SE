---
description: Huvudvyn består av den zoombara bilden.
seo-description: Huvudvyn består av den zoombara bilden.
seo-title: Zoomvy
solution: Experience Manager
title: Zoomvy
topic: Dynamic media
uuid: 06464e36-8c9c-4d3c-b4e5-5911f002568c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Zoomvy{#zoom-view}

Huvudvyn består av den zoombara bilden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7basiczoomviewer .s7zoomview
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
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

I skrivbordssystem stöder komponenten attributväljaren `cursortype` som kan tillämpas på klassen `.s7zoomview` och styr markörtypen baserat på komponentens tillstånd och användaråtgärd. Följande `cursortype`-värden stöds:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Värde </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> standard  </span> </p> </td> 
   <td colname="col2"> <p>Visas när bilden inte kan zoomas på grund av en liten bildupplösning, eller komponentinställningar, eller båda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin  </span> </p> </td> 
   <td colname="col2"> <p>Visas när bilden kan zoomas in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> återställ  </span> </p> </td> 
   <td colname="col2"> <p>Visas när bilden har maximal zoomnivå och kan återställas till det ursprungliga läget. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dra  </span> </p> </td> 
   <td colname="col2"> <p>Visas när en användare panorerar bilden som är i zoomläge. </p> </td> 
  </tr> 
 </tbody> 
</table>

