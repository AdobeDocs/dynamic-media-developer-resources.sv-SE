---
title: Verktygstips
description: På stationära datorer har vissa element i användargränssnittet, som knappar, verktygstips som visas när du hovrar musen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0350bdbc-3e3d-4bc0-98f6-5d7bf4121d9a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Verktygstips{#tooltips}

På stationära datorer har vissa element i användargränssnittet, som knappar, verktygstips som visas när du hovrar musen.

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
>Om verktygstipstipsen anpassas från inbäddningswebbsidan måste alla egenskaper innehålla regeln `!IMPORTANT`. Den här regeln är inte nödvändig om funktionsbeskrivningar har anpassats i visningsprogrammets CSS-fil.

Exempel - Om du vill ställa in verktygstips som har en grå kant med hörnradie 3 pixlar, svart bakgrund och vit text skriven med Arial®, 11 pixlar:

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
