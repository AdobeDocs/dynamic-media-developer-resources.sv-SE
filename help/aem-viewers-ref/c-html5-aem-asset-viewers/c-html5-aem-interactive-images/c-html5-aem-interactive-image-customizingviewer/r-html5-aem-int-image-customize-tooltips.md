---
description: På stationära datorer har vissa element i användargränssnittet, som knappar, verktygstips som visas när du hovrar musen.
seo-description: På stationära datorer har vissa element i användargränssnittet, som knappar, verktygstips som visas när du hovrar musen.
seo-title: Verktygstips
solution: Experience Manager
title: Verktygstips
topic: Dynamic media
uuid: 4cf5ce32-136e-4612-b550-715d51cef982
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

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
   <td colname="col2"> <p> Bakgrundsfärg. </p> </td> 
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
   <td colname="col2"> <p>Teckensnittsstorlek för text. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Om verktygstipstipsen anpassas från webbsidan för inbäddning måste alla egenskaper innehålla `!IMPORTANT` regler. Detta är inte nödvändigt om verktygstipsen är anpassade i visningsprogrammets CSS-fil.

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

