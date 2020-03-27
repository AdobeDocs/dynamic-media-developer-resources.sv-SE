---
description: Markering av indatafokus som visas runt element i användargränssnittet för fokuserade visningsprogram styrs med CSS-klassväljaren.
seo-description: Markering av indatafokus som visas runt element i användargränssnittet för fokuserade visningsprogram styrs med CSS-klassväljaren.
seo-title: Fokusmarkering
solution: Experience Manager
title: Fokusmarkering
topic: Dynamic media
uuid: 99d822b5-29ea-4229-8eb8-e3903322b7fa
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

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
   <td colname="col1"> <p> <span class="codeph"> kontur </span> </p> </td> 
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

