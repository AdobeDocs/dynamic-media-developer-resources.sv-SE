---
description: Visningsprogrammet visar sökresultatområden över huvudvyn så att ord eller fraser som finns i katalogen markeras.
seo-description: Visningsprogrammet visar sökresultatområden över huvudvyn så att ord eller fraser som finns i katalogen markeras.
seo-title: Sökeffekt
solution: Experience Manager
title: Sökeffekt
topic: Dynamic Media
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Sökeffekt{#search-effect}

Visningsprogrammet visar sökresultatområden över huvudvyn så att ord eller fraser som finns i katalogen markeras.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Utseendet på sökresultatregioner styrs med följande CSS-klassväljare:

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p>Bakgrund för sökresultatområdet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in sökresultatområden med en halvgenomskinlig, gul fyllning:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

