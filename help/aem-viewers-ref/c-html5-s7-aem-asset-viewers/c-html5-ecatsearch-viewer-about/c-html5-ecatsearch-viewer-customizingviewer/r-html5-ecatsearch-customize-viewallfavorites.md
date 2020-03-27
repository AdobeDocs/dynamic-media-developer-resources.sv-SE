---
description: Knappens position hanteras helt av Favoriter-menyn.
seo-description: Knappens position hanteras helt av Favoriter-menyn.
seo-title: Knappen Visa alla favoriter
solution: Experience Manager
title: Knappen Visa alla favoriter
topic: Dynamic media
uuid: 8824deb5-3bdc-4681-85ac-7f86a76cf3b5
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Knappen Visa alla favoriter{#view-all-favorites-button}

Knappens position hanteras helt av Favoriter-menyn.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Utseendet på knappen Visa alla favoriter styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7viewallfavoritebutton
```

**CSS-egenskaper för knappen Ta bort favorit**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knappens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Knappens höjd. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för både `state` - och `selected` attributväljare, som kan användas för att tillämpa olika skal på olika knapplägen. Motsvarar i synnerhet läget när en användare kan lägga till en ny Favorit-ikon genom att klicka eller trycka på. `selected='true'` `selected='false'` motsvarar det normala driftsläget när en användare kan zooma, panorera och byta sidor.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - om du vill ställa in knappen Visa alla favoriter som är 28 x 28 pixlar och visar en annan bild för var och en av de fyra olika knapplägena när den är markerad eller inte markerad.

```
.s7ecatalogsearchviewer .s7viewallfavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7viewallfavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7viewallfavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7viewallfavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7viewallfavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_disabled.png); 
} 
.s7ecatalogsearchviewer .s7viewallfavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7viewallfavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7viewallfavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7viewallfavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_disabled.png); 
}
```

