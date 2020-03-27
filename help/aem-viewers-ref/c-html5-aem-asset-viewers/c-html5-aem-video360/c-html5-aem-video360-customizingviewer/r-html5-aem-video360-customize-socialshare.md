---
description: Verktyget för delning via sociala medier visas som standard i det övre högra hörnet. Den består av en knapp och en panel som utökas när användaren klickar eller trycker på en knapp och innehåller enskilda delningsverktyg.
seo-description: Verktyget för delning via sociala medier visas som standard i det övre högra hörnet. Den består av en knapp och en panel som utökas när användaren klickar eller trycker på en knapp och innehåller enskilda delningsverktyg.
seo-title: Social andel
solution: Experience Manager
title: Social andel
topic: Dynamic media
uuid: d7b7e704-6f78-45f9-a82a-14dc6b01e230
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Social andel{#social-share}

Verktyget för delning via sociala medier visas som standard i det övre högra hörnet. Den består av en knapp och en panel som utökas när användaren klickar eller trycker på en knapp och innehåller enskilda delningsverktyg.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Placeringen och storleken på verktyget för delning via sociala medier i visningsprogrammets användargränssnitt styrs med följande:

```
.s7video360viewer .s7socialshare
```

**CSS-egenskaper för verktyget för social delning**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Det sociala delningsverktygets lodräta position i förhållande till visningsprogrambehållaren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster </span> </p> </td> 
   <td colname="col2"> <p> Vågrät position för verktyget för delning via sociala medier i förhållande till visningsprogrambehållaren. </p> </td> 
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

**Exempel** - Om du vill ställa in ett verktyg för delning via sociala medier som är placerat fyra pixlar från överkanten och fem pixlar från höger om visningsprogrammets behållare och som är 28 x 28 pixlar stort.

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

Utseendet på verktygsknappen för delning via sociala medier styrs av följande CSS-klassväljare:

```
.s7video360viewer .s7socialshare .s7socialbutton
```

**CSS-egenskaper för verktygsknappen för delning via sociala medier**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Knappens funktionsbeskrivning kan lokaliseras. Se [Lokalisering av element](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)i användargränssnittet.

**Exempel** - Om du vill ställa in en knapp för verktyget för delning via sociala medier som visar olika bilder för de fyra olika knapplägena.

```
.s7video360viewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

Utseendet på panelen som innehåller de enskilda ikonerna för social delning styrs med följande CSS-klassväljare:

```
.s7video360viewer .s7socialshare .s7socialsharepanel
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

**Exempel** - Så här ställer du in en panel med genomskinlig färg:

```
.s7video360viewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

