---
description: Huvudvyn består av rotationsbilden när den aktuella resursen är en snurruppsättning.
seo-description: Huvudvyn består av rotationsbilden när den aktuella resursen är en snurruppsättning.
seo-title: Vyn Snurra
solution: Experience Manager
title: Vyn Snurra
topic: Dynamic media
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Vyn Snurra{#spin-view}

Huvudvyn består av rotationsbilden när den aktuella resursen är en snurruppsättning.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col2"> <p> Bakgrundsfärg i hexadecimalt format för rotationsvyn. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill göra rotationsvyn genomskinlig.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

