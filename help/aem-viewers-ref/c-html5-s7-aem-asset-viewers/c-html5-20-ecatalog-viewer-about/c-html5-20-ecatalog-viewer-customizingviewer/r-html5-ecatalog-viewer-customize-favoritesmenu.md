---
description: Listrutan Favoriter visas i kontrollfältet. Den består av en knapp och en panel som utökas när en användare klickar eller trycker på en knapp. Panelen innehåller enskilda favoritverktyg.
seo-description: Listrutan Favoriter visas i kontrollfältet. Den består av en knapp och en panel som utökas när en användare klickar eller trycker på en knapp. Panelen innehåller enskilda favoritverktyg.
seo-title: Favoriter-menyn
solution: Experience Manager
title: Favoriter-menyn
topic: Dynamic media
uuid: 816e614d-8253-49a8-b57e-0b57b44db535
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Favoritmeny{#favorites-menu}

Listrutan Favoriter visas i kontrollfältet. Den består av en knapp och en panel som utökas när en användare klickar eller trycker på en knapp. Panelen innehåller enskilda favoritverktyg.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Placeringen och storleken på Favoriter-menyn i visningsprogrammets användargränssnitt styrs med följande CSS-klassväljare:

```
.s7ecatalogviewer .s7favoritesmenu
```

**CSS-egenskaper för menyknappen Favoriter**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-top  </span> </p> </td> 
   <td colname="col2"> <p> Förskjutningen från kontrollfältets överkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-vänster  </span> </p> </td> 
   <td colname="col2"> <p> Avståndet till nästa knapp till vänster eller till vänster om kontrollfältet om det är den första knappen på en rad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knappens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Knappens höjd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - Ställ in en Favoriter-meny som är placerad fyra pixlar från kontrollfältets överkant och tio pixlar från den närmaste knappen till vänster och som har storleken 28 x 28 pixlar.

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

Utseendet på menyknappen Favoriter styrs av följande CSS-klassväljare:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

**CSS-egenskaper för knappen Favoriter**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder attributväljaren `state`, som kan användas för att tillämpa olika skal på olika knapplägen.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exempel - Ställ in en Favoriter-menyknapp som visar olika bilder för de fyra olika knapplägena.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

Utseendet på panelen som innehåller enskilda Favoriter-ikoner styrs av följande CSS-klassväljare:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**CSS-egenskaper i panelen Favoriter**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Panelens bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ange att en panel ska ha en genomskinlig färg.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

