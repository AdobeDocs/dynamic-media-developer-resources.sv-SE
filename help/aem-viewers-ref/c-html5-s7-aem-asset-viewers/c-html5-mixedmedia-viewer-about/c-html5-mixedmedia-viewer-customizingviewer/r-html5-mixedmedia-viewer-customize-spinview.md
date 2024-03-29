---
title: Vyn Snurra
description: Huvudvyn består av rotationsbilden när den aktuella resursen är en snurruppsättning.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

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

Exempel - Om du vill göra rotationsvyn genomskinlig.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
