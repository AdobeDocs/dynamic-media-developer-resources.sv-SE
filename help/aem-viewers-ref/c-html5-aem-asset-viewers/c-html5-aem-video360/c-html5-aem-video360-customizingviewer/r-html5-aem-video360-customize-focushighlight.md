---
title: Fokusmarkering
description: Markering av indatafokus som visas runt element i användargränssnittet för fokuserade visningsprogram styrs med CSS-klassväljaren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 05ac1a70-c20d-4ddf-942c-181f101cb1d8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Fokusmarkering{#focus-highlight}

Markering av indatafokus som visas runt element i användargränssnittet för fokuserade visningsprogram styrs med CSS-klassväljaren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper**

Utseendet styrs med följande CSS-klassväljare:

```
.s7video360viewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> kontur  </span> </p> </td> 
   <td colname="col2"> <p>Fokusmarkeringsstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - Om du vill inaktivera standardmarkeringen för webbläsarfokus för alla element i visningsprogrammets användargränssnitt lägger du till följande CSS-väljare i visningsprogrammets formatmall:

```
.s7video360viewer *:focus { 
 outline: none; 
}
```
