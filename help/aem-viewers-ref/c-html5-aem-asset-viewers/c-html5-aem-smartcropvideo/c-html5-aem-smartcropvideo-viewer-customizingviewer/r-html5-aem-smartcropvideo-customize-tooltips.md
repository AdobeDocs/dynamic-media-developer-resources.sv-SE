---
title: Verktygstips
description: På stationära datorer har vissa element i användargränssnittet, t.ex. knappar, verktygstips som visas när du hovrar musen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 78cc0f11-bec2-495e-b3c9-a91b6bd1b1f0
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---

# Verktygstips{#tooltips}

På stationära datorer har vissa element i användargränssnittet, t.ex. knappar, verktygstips som visas när du hovrar musen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Utseendet på verktygstipsen styrs av följande CSS-klassväljare:

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Kantradie för bakgrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> Kantfärg för bakgrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärg </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Textfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Textteckensnittsnamn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek för text. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Om verktygstipsen anpassas från inbäddningswebbsidan måste alla egenskaper innehålla en `!IMPORTANT`-regel. Den här regeln är inte nödvändig om verktygstipsen är anpassade i visningsprogrammets CSS-fil.

Exempel - för att skapa verktygstips med en grå kant med hörnradie 3 pixlar, svart bakgrund och vit text skriven med Arial®, 11 pixlar:

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
