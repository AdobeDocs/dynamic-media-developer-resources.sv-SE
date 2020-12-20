---
description: I det textbundna zoomläget består huvudvyn av den statiska bilden, den zoomade bilden som visas i den utfällbara vyn över den statiska bilden och det tips som visas ovanpå den statiska bilden.
seo-description: I det textbundna zoomläget består huvudvyn av den statiska bilden, den zoomade bilden som visas i den utfällbara vyn över den statiska bilden och det tips som visas ovanpå den statiska bilden.
seo-title: Utfällbar zoomvy
solution: Experience Manager
title: Utfällbar zoomvy
topic: Dynamic media
uuid: c4c94432-7b6f-40a8-ae5f-9423234f3656
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# Utfällbar zoomvy{#flyout-zoom-view}

I det textbundna zoomläget består huvudvyn av den statiska bilden, den zoomade bilden som visas i den utfällbara vyn över den statiska bilden och det tips som visas ovanpå den statiska bilden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Utseendet på huvudvyn styrs med följande CSS-klassväljare:

```
.s7mixedmediaviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Huvudvyns bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att göra huvudvyn genomskinlig:

```
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

Utseendet på tipsmeddelandet styrs av följande CSS-klassväljare:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

Det går att konfigurera teckensnittsstil, storlek och lodrät förskjutning via CSS. Den vågräta justeringen hanteras emellertid av visningsprogrammets logik. Det går inte att åsidosätta den via CSS med egenskaperna `left` eller `right`.

**CSS-egenskaper för tipsmeddelandet**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Fyllningsfärg för meddelandebakgrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Kantradie för meddelandebakgrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant  </span> </p> </td> 
   <td colname="col2"> <p> Förskjutning längst ned i huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg  </span> </p> </td> 
   <td colname="col2"> <p>Tips för textfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsfamilj. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacitet  </span> </p> </td> 
   <td colname="col2"> <p> Ogenomskinlighet för meddelandebakgrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p> Utfyllnad runt meddelandetexten. </p> </td> 
  </tr> 
 </tbody> 
</table>

Tipsmeddelandet kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Exempel - Om du vill ange ett halvgenomskinligt tips med vitt Arial 12px-teckensnitt, förskjuts 50 pixlar från huvudvyns nederkant, utfyllnad och en rundad kant:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```

