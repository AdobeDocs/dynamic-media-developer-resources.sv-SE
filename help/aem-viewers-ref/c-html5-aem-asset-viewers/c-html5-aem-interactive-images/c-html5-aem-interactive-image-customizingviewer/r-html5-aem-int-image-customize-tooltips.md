---
title: Verktygstips
description: På stationära datorer har vissa element i användargränssnittet, som knappar, verktygstips som visas när du hovrar musen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 25d4aa58-e16e-4b96-bca0-e98d542b7b81
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
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
>Om verktygstipstipsen anpassas från inbäddningswebbsidan måste alla egenskaper innehålla regeln `!IMPORTANT`. Detta är inte nödvändigt om verktygstipsen är anpassade i visningsprogrammets CSS-fil.

Exempel - för att ställa in funktionsbeskrivningar som har en grå kant med en hörnradie på 3 pixlar, svart bakgrund och vit text i Arial, 11 pixlar stor:

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
