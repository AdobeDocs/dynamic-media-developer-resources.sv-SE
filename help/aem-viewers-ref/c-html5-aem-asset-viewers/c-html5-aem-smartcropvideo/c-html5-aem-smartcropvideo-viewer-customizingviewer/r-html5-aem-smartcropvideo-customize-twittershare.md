---
title: Twitter
description: Twitter delningsverktyg består av en knapp som läggs till på panelen Dela via sociala medier. När knappen är markerad dirigeras användaren om till en delningsdialogruta som tillhandahålls av en social tjänst. Knappens position hanteras helt av verktyget för social delning.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5bcf6868-7ebb-43ec-971d-2be9e53650bb
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Twitter{#twitter-share}

Twitter delningsverktyg består av en knapp som läggs till på panelen Dela via sociala medier. När knappen är markerad dirigeras användaren om till en delningsdialogruta som tillhandahålls av en social tjänst. Knappens position hanteras helt av verktyget för social delning.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Utseendet på Twitter-delningsknappen styrs av följande CSS-klassväljare:

```
.s7smartcropvideoviewer .s7twittershare
```

**CSS-egenskaper för delningsverktyget i Twitter**

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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för `state` attributväljare, som kan användas för att tillämpa olika skal på olika knapplägen.

Det går att ta bort knappen från panelen Dela via inställningen `display:none` CSS-egenskap i dess CSS-klass.

Knappens funktionsbeskrivning kan lokaliseras. Se [Lokalisering av användargränssnittselement](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) för mer information.

Exempel - för att ställa in en delningsknapp på Twitter som är 28 x 28 pixlar och visar en annan bild för vart och ett av de fyra olika knapplägena:

```
.s7smartcropvideoviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
