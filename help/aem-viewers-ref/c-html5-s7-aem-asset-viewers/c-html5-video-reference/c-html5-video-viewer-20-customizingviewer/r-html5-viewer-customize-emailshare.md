---
description: Verktyget för e-postdelning består av en knapp som läggs till på panelen Dela via sociala medier och i den modala dialogrutan som visas när verktyget aktiveras. Knappens position hanteras helt av verktyget för social delning.
seo-description: Verktyget för e-postdelning består av en knapp som läggs till på panelen Dela via sociala medier och i den modala dialogrutan som visas när verktyget aktiveras. Knappens position hanteras helt av verktyget för social delning.
seo-title: E-postresurs
solution: Experience Manager
title: E-postresurs
topic: Dynamic media
uuid: 4c6abb74-7e13-4fed-bbfb-45e388627578
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# E-postresurs{#email-share}

Verktyget för e-postdelning består av en knapp som läggs till på panelen Dela via sociala medier och i den modala dialogrutan som visas när verktyget aktiveras. Knappens position hanteras helt av verktyget för social delning.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Utseendet på e-postdelningsknappen styrs av följande CSS-klassväljare:

```
.s7videoviewer .s7emailshare
```

**CSS-egenskaper för e-postdelningsverktyget**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knappens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Knappens höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Det går att ta bort knappen från panelen för sociala medier genom att ange `display:none` CSS-egenskapen i dess CSS-klass.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Exempel - för att ställa in en knapp för e-postdelning som är 28 x 28 pixlar och som visar en annan bild för vart och ett av de fyra olika knapplägena.

```
.s7videoviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7videoviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7videoviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7videoviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

Bakgrundsöverlägget som täcker webbsidan när dialogrutan är aktiv styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7backoverlay
```

**CSS-egenskaper för bakåtövertäckningen**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacitet </span> </p> </td> 
   <td colname="col2"> <p> Opacitet för bakgrundsövertäckning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsövertäckningsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in bakgrundsövertäckningen till grått med 70 % opacitet:

```
.s7videoviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Som standard visas den modala dialogrutan centrerat på skärmen på stationära datorer och tar hela webbsidans område på pekenheter. I samtliga fall hanteras placeringen och storleken på dialogrutan av komponenten. Dialogrutan styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialog
```

**CSS-egenskaper i dialogrutan**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Dialogrutans kantradie (om dialogrutan inte tar hela webbläsarfönstret). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Dialogrutans bakgrundsfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> ska antingen vara urkopplad eller inställd på 100 %, i vilket fall dialogrutan tar hela webbläsarfönstret (detta läge rekommenderas på pekenheter), </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Ska antingen vara unset eller inställd på 100 %, vilket innebär att dialogrutan visas i hela webbläsarfönstret (det här läget rekommenderas på enheter med pekskärm). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in dialogrutan så att hela webbläsarfönstret används och den har vit bakgrund på pekenheter:

```
.s7videoviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Dialogrutans rubrik består av en ikon, en titeltext och en stängningsknapp. Rubrikbehållaren styrs med följande CSS-klassväljare

```
.s7videoviewer .s7emaildialog .s7dialogheader
```

**CSS-egenskaper för dialogrutans rubrik**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p> Inre utfyllnad för rubrikinnehåll. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ikonen och rubriktexten placeras i en extra behållare som styrs med

```
.s7videoviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**CSS-egenskaper för dialograden**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p> Inre utfyllnad för rubrikikonen och titeln </p> </td> 
  </tr> 
 </tbody> 
</table>

Rubrikikonen styrs med följande CSS-klassväljare

```
.s7videoviewer .s7emaildialog .s7dialogheadericon
```

**CSS-egenskaper för dialogrutans rubrikikon**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ikonens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Ikonhöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Ikonbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Rubriken styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogheadertext
```

**CSS-egenskaper för rubriktexten i dialogrutan**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Teckenbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenhöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsfamilj. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Intern textutfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Stängningsknappen styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7closebutton
```

**CSS-egenskaper för stängningsknappen **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Lodrät knappposition i förhållande till rubrikbehållare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger </span> </p> </td> 
   <td colname="col2"> <p> Vågrät knappposition i förhållande till rubrikbehållare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knappbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Knapphöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Knappens inre utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Knappbild för varje läge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Knappbeskrivningen Stäng och dialogrutans titel kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Exempel - för att ställa in dialoghuvud med utfyllnad, ikon med storleken 24 x 17 pixlar, fet 16 punkters titel och stängningsknapp med storleken 28 x 28 pixlar, placerad 2 pixlar uppifrån och 2 pixlar från höger i dialogrutan:

```
.s7videoviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Sidfoten i dialogrutan består av knapparna Avbryt och Skicka e-post. Sidfotsbehållaren styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogfooter
```

**CSS-egenskaper för dialogrutans sidfot **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> Kant som kan användas för att visuellt separera sidfoten från resten av dialogrutan. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sidfoten har en inre behållare som behåller båda knapparna. Den styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogbuttoncontainer
```

**CSS-egenskaper för behållaren för dialogruteknappen**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p> Inre utfyllnad mellan sidfoten och knapparna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Knappen Avbryt styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogcancelbutton
```

**CSS-egenskaper för knappen Avbryt i dialogrutan**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
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
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p> Knapptextfärg för varje läge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Knappbakgrundsfärg för varje läge. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Knappen Skicka e-post styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogactionbutton
```

**CSS-egenskaper för dialogrutans åtgärdsknapp**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p> Knapptextfärg för varje läge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Knappbakgrundsfärg för varje läge. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Dessutom har båda knapparna samma gemensamma CSS-klass som kan innehålla CSS-inställningar som är desamma för andra dialogruteknappar:

```
.s7videoviewer .s7emaildialog .s7dialogfooter .s7button
```

**CSS-egenskaper för knappen**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Knappens teckensnittsbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Knappens teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Knappteckensnittsfamilj. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> Texthöjd inuti knappen. Påverkar lodrät justering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>Skugga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-höger </span> </p> </td> 
   <td colname="col2"> <p>Högerknappsmarginal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Knappverktygstipsen kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Exempel - om du vill ställa in en dialogruteslut med knappen Avbryt 64 x 34 och skicka e-postknappen 82 x 34, med textfärgen och bakgrundsfärgen olika för varje knappläge:

```
.s7videoviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Huvuddialogrutan (mellan sidhuvudet och sidfoten) innehåller rullningsbart dialogruteinnehåll och rullningspanelen till höger. I samtliga fall hanterar komponenten bredden på det här området, det går inte att ange den i CSS. Huvudområdet i dialogrutan styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogviewarea
```

**CSS-egenskaper i dialogrutans visningsområde **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Höjden på området i huvuddialogrutan. Den ska bara anges när dialogrutan fungerar i skrivbordsläge. Det är inte tillämpligt när dialogrutans storlek ändras så att den upptar hela webbläsarfönstret. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärgen i huvuddialogrutan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p>Yttre marginal. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Huvuddialogrutan har stöd för den valfria `state` attributväljaren. Den ställs in på `sendsuccess` när e-postformuläret skickas och dialogrutan visar ett bekräftelsemeddelande. Så länge bekräftelsemeddelandet är litet kan den här attributväljaren användas för att minska dialogrutans höjd när ett sådant bekräftelsemeddelande visas.

Exempel - Om du vill ställa in att huvudområdet i dialogrutan ska vara 300 pixlar högt från början och 100 pixlar högt när bekräftelsemeddelandet visas, har du en marginal på tio pixlar och använder en vit bakgrund:

```
.s7videoviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7videoviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

Allt formulärinnehåll (som etiketter och inmatningsfält) finns inuti en behållare som styrs med

```
.s7videoviewer .s7emaildialog .s7dialogbody
```

Om höjden på den här behållaren verkar vara större än huvudområdet i dialogrutan aktiveras en lodrät rullning automatiskt av komponenten.

**CSS-egenskaper för dialogrutans brödtext **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in formulärinnehåll så att det har utfyllnad på tio pixlar:

```
.s7videoviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

Dialogruteformuläret fylls i rad för rad, där varje rad innehåller en del av formulärinnehållet (som en etikett och ett textinmatningsfält). En formulärrad styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**CSS-egenskaper för dialograden**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Utfyllnad för inre linje. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in ett dialogruteformulär så att det får tio pixlar för varje rad:

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

Alla statiska etiketter i dialogruteformuläret styrs med

```
.s7videoviewer .s7emaildialog .s7dialoglabel
```

Den här klassen är inte lämplig för att styra etikettens storlek eller placering eftersom du kan använda den på text på olika ställen i användargränssnittet.

**CSS-egenskaper för dialogruteetiketten. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Etikettens teckensnittsbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsstorlek för etikett. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Etikettteckensnittsfamilj. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Textfärg för etikett. </p> </td> 
  </tr> 
 </tbody> 
</table>

Dialogruteetiketterna kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Exempel - om du vill ställa in alla etiketter till grått, fet med ett teckensnitt på nio pixlar:

```
.s7videoviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Alla statiska etiketter som visas till vänster om formulärinmatningsfälten styrs med:

```
.s7videoviewer .s7emaildialog .s7dialoginputlabel
```

**CSS-egenskaper för dialogrutans indataetikett**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredden på den statiska etiketten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> textjustering </span> </p> </td> 
   <td colname="col2"> <p>Den vågräta textjusteringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p>Statisk etikettmarginal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Statisk etikettutfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in etiketter för inmatningsfält så att de är 50 pixlar breda, högerjusterade, har tio pixlar utfyllnad och en marginal på tio pixlar till höger:

```
.s7videoviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

Varje formulärindatafält placeras i behållaren så att du kan använda en anpassad kantlinje runt indatafältet. Den styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialoginputcontainer
```

**CSS-egenskaper för dialogrutans indatabehållare**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Kant runt inmatningsfältbehållaren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Indatafältbehållaren stöder valfri `state` attributväljare. Den ställs in på `verifyerror` när användaren gör ett misstag i indataformatet och den interna valideringen misslyckas. Den här attributväljaren kan användas för att markera felaktiga användarindata i formuläret.

De flesta indatafält som sprids från etiketten till vänster upp till höger i dialogrutans brödtext (som innehåller fältet&quot;from&quot; och&quot;message&quot;) styrs med:

```
.s7videoviewer .s7emaildialog .s7dialoginputwide
```

**CSS-egenskaper för dialogrutans inmatningsfält**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på indatafält. </p> </td> 
  </tr> 
 </tbody> 
</table>

Indatafältet &quot;Till&quot; är smalare eftersom det tilldelar utrymme för knappen &quot;Ta bort e-post&quot; till höger. Den styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialoginputshort
```

**CSS-egenskaper för dialogrutans korta inmatningsfält**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på indatafält. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - att ställa in ett formulär så att det har en grå kant på en pixel med nio pixlar utfyllnad runt alla inmatningsfält. att ha samma kantlinje i röd färg för fält som inte godkänns vid validering, att ha indatafältet &quot;Till&quot; som är 250 pixlar brett och resten av inmatningsfälten 300 pixlar brett:

```
.s7videoviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

Indatafältet för e-postmeddelanden styrs dessutom med:

```
.s7videoviewer .s7emaildialog .s7dialogmessage
```

Med den här klassen kan du ange specifika egenskaper för det underliggande `TEXTAREA` elementet.

**CSS-egenskaper för dialogrutemeddelandet**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Meddelandets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap </span> </p> </td> 
   <td colname="col2"> <p>Radbrytningsformat. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ange att ett e-postmeddelande ska vara 50 pixlar högt och använda `break-word` automatisk radbrytning:

```
.s7videoviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

Med knappen Lägg till en annan e-postadress kan användaren lägga till fler än en adress i e-postformuläret. Den styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton
```

**CSS-egenskaper i dialogrutan lägger till e-postadressknapp**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Knapphöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Knapptextfärg för varje läge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Knappbild för varje läge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Knappbildens placering inuti knappområdet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Knappens teckensnittsbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Knappens teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Knappteckensnittsfamilj. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Texthöjd inuti knappen. Påverkar den lodräta justeringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> textjustering </span> </p> </td> 
   <td colname="col2"> <p>Vågrät textjustering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Exempel - Om du vill ställa in knappen &quot;Lägg till en annan e-postadress&quot; så att den är 25 pixlar hög använder du 12 punkters fet stil med högerjustering och en annan textfärg och bild för varje läge:

```
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

Med knappen &quot;Ta bort&quot; kan en användare ta bort extra adresser från e-postformuläret. Den styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton
```

**CSS-egenskaper för dialogrutan Ta bort e-postknapp**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
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
   <td colname="col2"> <p>Knappbild för varje läge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Exempel - om du vill ställa in en&quot;Ta bort&quot;-knapp på 25 x 25 pixlar och använda olika bilder för varje läge:

```
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

Innehållet som delas visas längst ned i dialogrutan och innehåller en miniatyrbild, rubrik, ursprungs-URL och beskrivning. Förpackningen är förpackad i en behållare som är kontrollerad med:

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**CSS-egenskaper för dialogrutans innehåll **

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Behållarkanten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en behållare längst ned så att den har en prickad kant på en pixel och ingen utfyllnad:

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

Miniatyrbilder styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogthumbnail
```

Egenskapen `background-image` anges av komponentlogiken.

**CSS-egenskaper för dialogrutans miniatyrbild**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på miniatyrbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjd på miniatyrbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> lodrät justering </span> </p> </td> 
   <td colname="col2"> <p>Miniatyrbild för lodrät justering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en miniatyrbild som är 90 x 60 pixlar och en överkant som är justerad med tio pixlar utfyllnad:

```
.s7videoviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

Innehållsrubrik, ursprung och beskrivning grupperas ytterligare i en panel till höger om miniatyrbilden. Den styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialoginfopanel
```

**CSS-egenskaper för informationspanelen i dialogrutan**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Panelbredd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en innehållspanel som är 300 pixlar bred:

```
.s7videoviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

Innehållstiteln styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogtitle
```

**CSS-egenskaper för dialogrutans rubrik**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p>Yttre marginal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Teckenbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsfamilj. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en innehållstitel så att den använder fet stil och har en marginal på tio pixlar:

```
.s7videoviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

Innehållets ursprung styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogorigin
```

**CSS-egenskaper för dialogrutans innehållsursprung **

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p>Yttre marginal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Teckenbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsfamilj. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in innehållets utgångspunkt så att den har en marginal på tio pixlar:

```
.s7videoviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

Innehållsbeskrivningen styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogdescription
```

**CSS-egenskaper för dialogrutans innehållsbeskrivning**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p>Yttre marginal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Teckenbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsfamilj. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en innehållsbeskrivning så att den har en marginal på tio pixlar och ett teckensnitt med nio punkter:

```
.s7videoviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

När en användare anger felaktiga indata och intern validering misslyckas, eller när dialogrutan behöver visa ett fel eller ett bekräftelsemeddelande när formuläret skickas, visas ett meddelande högst upp i dialogrutan. Den styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogerrormessage
```

**CSS-egenskaper i dialogrutans felmeddelande**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Felikon. Standard är ett utropstecken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Felikonens position i meddelandeområdet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Textfärg för meddelande. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Teckenbredd. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> Texthöjd inuti meddelandet. Påverkar lodrät justering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Det här meddelandet har stöd för attributväljaren med följande möjliga värden: `state` `verifyerror`, `senderror`och `sendsuccess`. `verifyerror` anges när ett meddelande visas på grund av ett internt indatavalideringsfel. `senderror` ställs in när en backend-e-posttjänst rapporterar ett fel, anges `sendsuccess` när e-post skickas. På det här sättet kan du formatera meddelandet på olika sätt beroende på hur dialogrutan ser ut.

Felmeddelandet kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Exempel - om du vill ange att ett meddelande ska använda ett teckensnitt med 10 punkter fet stil, har radhöjden 25 pixlar, utfyllnaden 20 pixlar till vänster, använder ett utropstecken, röd text om ett fel uppstår och ingen ikon och grön text om det lyckas:

```
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

Om lodrät rullning behövs återges rullningslisten i panelen nära den högra kanten av dialogrutan, som styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7dialogscrollpanel
```

**CSS-egenskaper för dialogrutans rullningspanel**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på rullningspanelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in en rullningspanel till 44 pixlar bred:

```
.s7videoviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

Utseendet på rullningslistområdet styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7scrollbar
```

**CSS-egenskaper för rullningslisten**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på rullningslisten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Den lodräta rullningslistens förskjutning från rullningspanelens överkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p> Den lodräta rullningslistens förskjutning från rullningspanelens nederkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger </span> </p> </td> 
   <td colname="col2"> <p> Den vågräta rullningslistens förskjutning från rullningspanelens högra kant. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in en rullningslist som är 28 pixlar bred, en åtta pixelmarginaler uppifrån, till höger och nedåt på rullningspanelen:

```
.s7videoviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Rullningslistens spår är området mellan den övre och den nedre rullningsknappen. Komponenten ställer automatiskt in spårets position och höjd. Spåret styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**CSS-egenskaper för rullningsspåret**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Spårbredden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärgen för spåret. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in ett rullningslistspår som är 28 pixlar brett och har en grå bakgrund:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Rullningslistens reglage rör sig lodrätt inom ett rullningsspårsområde. Dess lodräta position styrs helt av komponentlogiken, men tumhöjden ändras inte dynamiskt beroende på mängden innehåll. Du kan konfigurera tumhöjden och andra aspekter med följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**CSS-egenskaper för rullningslistens reglage**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Miniatyrbredden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Tumthöjden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p> Den lodräta utfyllnaden mellan spårets överkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> Den lodräta utfyllnaden mellan spårets nederkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Bilden som visas för ett givet tumläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tummen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika tumlägen: `state` `up`, `down`, `over`och `disabled`.

Knappverktygstipsen kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Exempel - för att ställa in rullningslistens reglage som är 28 x 45 pixlar, har en marginal på tio pixlar över och under och har olika teckningar för varje läge:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

Utseendet på de övre och nedre rullningsknapparna styrs av följande CSS-klassväljare:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton  
  
```

**CSS-egenskaper för de övre och nedre rullningsknapparna**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knappens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Knappens höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Dessa knappar har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen: `state` `up`, `down`, `over`och `disabled`.

Exempel - för att ställa in rullningsknappar som är 28 x 32 pixlar och har olika teckningar för varje läge:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

