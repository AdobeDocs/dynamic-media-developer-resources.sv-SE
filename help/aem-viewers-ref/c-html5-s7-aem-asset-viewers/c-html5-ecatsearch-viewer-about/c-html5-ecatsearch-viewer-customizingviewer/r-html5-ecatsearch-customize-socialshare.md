---
description: Verktyget för social delning visas som standard i det övre vänstra hörnet. Den består av en knapp och en panel som utökas när användaren klickar eller trycker på en knapp och innehåller enskilda delningsverktyg.
seo-description: Verktyget för social delning visas som standard i det övre vänstra hörnet. Den består av en knapp och en panel som utökas när användaren klickar eller trycker på en knapp och innehåller enskilda delningsverktyg.
seo-title: Social andel
solution: Experience Manager
title: Social andel
topic: Dynamic media
uuid: 6d463eb1-c6bf-4f1c-90e4-b5ef1e5a1538
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Social andel{#social-share}

Verktyget för social delning visas som standard i det övre vänstra hörnet. Den består av en knapp och en panel som utökas när användaren klickar eller trycker på en knapp och innehåller enskilda delningsverktyg.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Placeringen och storleken på verktyget för delning via sociala medier i visningsprogrammets användargränssnitt styrs med följande:

```
.s7ecatalogsearchviewer .s7socialshare
```

**CSS-egenskaper för verktyget för social delning**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-top </span> </p> </td> 
   <td colname="col2"> <p> Förskjutningen från kontrollfältets överkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left </span> </p> </td> 
   <td colname="col2"> <p> Avståndet till nästa knapp till vänster eller till vänster om kontrollfältet om det är den första knappen på en rad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på verktyget för delning via sociala medier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på verktyget för delning via sociala medier. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - Ställ in ett verktyg för delning via sociala medier som är placerat fyra pixlar från överkanten och fem pixlar från höger om visningsprogrammets behållare och som har storleken 28 x 28 pixlar.

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

Utseendet på verktygsknappen för delning via sociala medier styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
```

**CSS-egenskaper för den sociala knappen**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - Ställ in en knapp för verktyget för delning via sociala medier som visar olika bilder för de fyra olika knapplägena.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

Utseendet på panelen som innehåller de enskilda ikonerna för social delning styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
```

**CSS-egenskaper för panelen för sociala medier**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Panelens bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ställ in en panel så att den har genomskinlig färg:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

