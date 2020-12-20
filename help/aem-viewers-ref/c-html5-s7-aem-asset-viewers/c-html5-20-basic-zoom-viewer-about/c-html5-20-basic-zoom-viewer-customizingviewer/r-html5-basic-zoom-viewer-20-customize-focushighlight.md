---
description: Markering av indatafokus som visas runt gränssnittselementet för fokuserat visningsprogram styrs med CSS-klassväljaren.
seo-description: Markering av indatafokus som visas runt gränssnittselementet för fokuserat visningsprogram styrs med CSS-klassväljaren.
seo-title: Fokusmarkering
solution: Experience Manager
title: Fokusmarkering
topic: Dynamic media
uuid: 1b552aec-837a-4df4-91dc-615ceead92b3
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---


# Fokusmarkering{#focus-highlight}

Markering av indatafokus som visas runt gränssnittselementet för fokuserat visningsprogram styrs med CSS-klassväljaren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Utseendet styrs med följande CSS-klassväljare:

```
.s7basiczoomviewer *:focus
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
.s7basiczoomviewer *:focus { 
 outline: none; 
}
```

