---
description: Verktyget för delning via sociala medier visas som standard i det övre högra hörnet. Den består av en knapp och en panel som utökas när användaren klickar eller trycker på en knapp och innehåller enskilda delningsverktyg.
seo-description: Verktyget för delning via sociala medier visas som standard i det övre högra hörnet. Den består av en knapp och en panel som utökas när användaren klickar eller trycker på en knapp och innehåller enskilda delningsverktyg.
seo-title: Social andel
solution: Experience Manager
title: Social andel
topic: Dynamic media
uuid: 5c1ce7b4-54bf-486f-8b57-1d6d0cec119e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---


# Social resurs{#social-share}

Verktyget för delning via sociala medier visas som standard i det övre högra hörnet. Den består av en knapp och en panel som utökas när användaren klickar eller trycker på en knapp och innehåller enskilda delningsverktyg.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Placeringen och storleken på verktyget för delning via sociala medier i visningsprogrammets användargränssnitt styrs med följande:

```
.s7videoviewer .s7socialshare
```

**CSS-egenskaper för verktyget för social delning**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Det sociala delningsverktygets lodräta position i förhållande till visningsprogrambehållaren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster  </span> </p> </td> 
   <td colname="col2"> <p> Vågrät position för verktyget för delning via sociala medier i förhållande till visningsprogrambehållaren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på verktyget för delning via sociala medier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höjden på verktyget för delning via sociala medier. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - Ställ in ett verktyg för delning via sociala medier som är placerat fyra pixlar från överkanten och fem pixlar från höger om visningsprogrammets behållare och som har storleken 28 x 28 pixlar.

```
.s7videoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

Utseendet på verktygsknappen för delning via sociala medier styrs av följande CSS-klassväljare:

```
.s7videoviewer .s7socialshare .s7socialbutton
```

**CSS-egenskaper för den sociala knappen**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder attributväljaren `state`, som kan användas för att tillämpa olika skal på olika knapplägen.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Exempel - Ställ in en knapp för verktyget för delning via sociala medier som visar olika bilder för de fyra olika knapplägena.

```
.s7videoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

Utseendet på panelen som innehåller de enskilda ikonerna för social delning styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7socialshare .s7socialsharepanel
```

**CSS-egenskaper för panelen för sociala medier**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Panelens bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ställ in en panel så att den har genomskinlig färg:

```
.s7videoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

