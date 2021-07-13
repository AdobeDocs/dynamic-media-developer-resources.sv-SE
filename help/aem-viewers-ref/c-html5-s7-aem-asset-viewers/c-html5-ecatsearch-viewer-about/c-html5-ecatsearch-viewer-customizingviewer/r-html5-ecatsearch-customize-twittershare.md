---
description: Twitter delningsverktyg består av en knapp som läggs till på panelen Dela via sociala medier. När användaren klickar på knappen omdirigeras användaren till en delningsdialogruta som tillhandahålls av en social tjänst. Knappens position hanteras helt av verktyget för social delning.
solution: Experience Manager
title: Twitter
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Developer,User
exl-id: c7e84d40-a779-4747-b79a-3a40a622a445
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Twitter{#twitter-share}

Twitter delningsverktyg består av en knapp som läggs till på panelen Dela via sociala medier. När användaren klickar på knappen omdirigeras användaren till en delningsdialogruta som tillhandahålls av en social tjänst. Knappens position hanteras helt av verktyget för social delning.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Utseendet på Twitter-delningsknappen styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7twittershare
```

**CSS-egenskaper för delningsverktyget i Twitter**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knappbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Knapphöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder attributväljaren `state`, som kan användas för att tillämpa olika skal på olika knapplägen.

Det går att ta bort knappen från panelen Dela via CSS-egenskapen `display:none` i CSS-klassen.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exempel - för att ställa in en delningsknapp på Twitter som är 28 x 28 pixlar och visar en annan bild för vart och ett av de fyra olika knapplägena:

```
.s7ecatalogsearchviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
