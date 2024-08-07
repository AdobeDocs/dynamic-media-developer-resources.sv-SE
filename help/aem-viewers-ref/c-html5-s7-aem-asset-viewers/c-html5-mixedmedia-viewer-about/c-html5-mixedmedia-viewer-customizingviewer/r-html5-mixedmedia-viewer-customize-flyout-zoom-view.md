---
title: Utfällbar zoomvy
description: I inline-zoomläget består huvudvyn av den statiska bilden. Den består också av den zoomade bilden som visas i den utfällbara vyn över den statiska bilden och det tips som visas ovanpå den statiska bilden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 46c91d1f-5809-4270-a06d-5068d20a6341
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Utfällbar zoomvy{#flyout-zoom-view}

I inline-zoomläget består huvudvyn av den statiska bilden. Den består också av den zoomade bilden som visas i den utfällbara vyn över den statiska bilden och det tips som visas ovanpå den statiska bilden.

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Fyllningsfärg för meddelandebakgrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Kantradie för meddelandebakgrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p> Förskjutning längst ned i huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Färg på tipstext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsfamilj. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacitet </span> </p> </td> 
   <td colname="col2"> <p> Ogenomskinlighet för meddelandebakgrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p> Utfyllnad runt meddelandetexten. </p> </td> 
  </tr> 
 </tbody> 
</table>

Tipsmeddelandet kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Exempel - Om du vill ange ett halvgenomskinligt tips med vitt Arial® 12-px-teckensnitt, förskjuts 50 pixlar från huvudvyns nederkant, utfyllnad och en rundad kant:

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
