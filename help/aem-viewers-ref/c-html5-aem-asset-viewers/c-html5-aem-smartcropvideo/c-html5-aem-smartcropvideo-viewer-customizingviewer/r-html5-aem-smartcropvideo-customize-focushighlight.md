---
title: Fokusmarkering
description: Markering av indatafokus som visas runt gränssnittselementet för fokuserade visningsprogram styrs med CSS-klassväljaren.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 242b80db-f5b4-44ad-9169-bd6ecf859ed0
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# Fokusmarkering{#focus-highlight}

Markering av indatafokus som visas runt gränssnittselementet för fokuserade visningsprogram styrs med CSS-klassväljaren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper**

Utseendet styrs med följande CSS-klassväljare:

```
.s7smartcropvideoviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> kontur </span> </p> </td> 
   <td colname="col2"> <p>Fokusmarkeringsstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - Om du vill inaktivera standardmarkeringen för webbläsarfokus för alla element i visningsprogrammets användargränssnitt lägger du till följande CSS-väljare i visningsprogrammets formatmall:

```
.s7smartcropvideoviewer *:focus { 
 outline: none; 
}
```
