---
description: Twitter-delningsverktyget består av en knapp som har lagts till på panelen Dela via sociala medier. När användaren klickar på knappen omdirigeras användaren till en delningsdialogruta som tillhandahålls av en social tjänst. Knappens position hanteras helt av verktyget för social delning.
seo-description: Twitter-delningsverktyget består av en knapp som har lagts till på panelen Dela via sociala medier. När användaren klickar på knappen omdirigeras användaren till en delningsdialogruta som tillhandahålls av en social tjänst. Knappens position hanteras helt av verktyget för social delning.
seo-title: Twitter-delning
solution: Experience Manager
title: Twitter-delning
topic: Dynamic media
uuid: 75b8eab1-74fd-4c18-8556-c3cb17011cde
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Twitter-delning{#twitter-share}

Twitter-delningsverktyget består av en knapp som har lagts till på panelen Dela via sociala medier. När användaren klickar på knappen omdirigeras användaren till en delningsdialogruta som tillhandahålls av en social tjänst. Knappens position hanteras helt av verktyget för social delning.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Utseendet på Twitter-delningsknappen styrs av följande CSS-klassväljare:

```
.s7ecatalogviewer .s7twittershare
```

**CSS-egenskaper för Twitter-delningsverktyget**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knappbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Knapphöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Det går att ta bort knappen från panelen för sociala medier genom att ange `display:none` CSS-egenskapen i dess CSS-klass.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - för att ställa in en Twitter-delningsknapp som är 28 x 28 pixlar och visar en annan bild för vart och ett av de fyra olika knapplägena:

```
.s7ecatalogviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7ecatalogviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7ecatalogviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7ecatalogviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```

