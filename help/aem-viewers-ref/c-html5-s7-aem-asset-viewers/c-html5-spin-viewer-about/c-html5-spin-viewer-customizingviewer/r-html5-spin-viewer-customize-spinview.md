---
description: Huvudvyn består av rotationsbilden.
solution: Experience Manager
title: Vyn Snurra
feature: Dynamic Media Classic,Visningsprogram,SDK/API,snurra uppsättningar
role: Developer,User
exl-id: d3274fe3-1a47-448e-acc6-6df77c6a4211
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---

# Vyn Snurra{#spin-view}

Huvudvyn består av rotationsbilden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Visningsområdets utseende styrs av följande CSS-klassväljare:

```
.s7spinviewer .s7spinview
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
 </tbody> 
</table>

Exempel - för att göra huvudvyn genomskinlig.

```
.s7spinviewer .s7spinview { 
 background-color: transparent; 
}
```
