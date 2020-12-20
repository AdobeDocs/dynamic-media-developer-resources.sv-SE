---
description: Länkdelningsverktyget består av en knapp som läggs till på panelen Dela via sociala medier och den modala dialogruta som visas när verktyget aktiveras. Knappens position hanteras helt av verktyget för social delning.
seo-description: Länkdelningsverktyget består av en knapp som läggs till på panelen Dela via sociala medier och den modala dialogruta som visas när verktyget aktiveras. Knappens position hanteras helt av verktyget för social delning.
seo-title: Länkresurs
solution: Experience Manager
title: Länkresurs
topic: Dynamic media
uuid: 699ddab2-8cfd-4edf-bb1b-5ff91fe63c1a
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1415'
ht-degree: 0%

---


# Länkresurs{#link-share}

Länkdelningsverktyget består av en knapp som läggs till på panelen Dela via sociala medier och den modala dialogruta som visas när verktyget aktiveras. Knappens position hanteras helt av verktyget för social delning.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Utseendet på knappen för länkdelning styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7linkshare
```

**CSS-egenskaper för länkdelningsverktyget**

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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder attributväljaren `state`, som kan användas för att tillämpa olika skal på olika knapplägen.

Det går att ta bort knappen från panelen Dela via CSS-egenskapen `display:none` i CSS-klassen.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Exempel - om du vill ställa in en knapp för länkdelning som är 28 x 28 pixlar och visar en annan bild för vart och ett av de fyra olika knapplägena:

```
.s7videoviewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7videoviewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7videoviewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7videoviewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

Bakgrundsöverlägget som täcker webbsidan när dialogrutan är aktiv styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7backoverlay
```

**CSS-egenskaper för bakgrundsövertäckningen**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacitet  </span> </p> </td> 
   <td colname="col2"> <p>Opacitet för bakgrundsövertäckning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsövertäckningsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en bakgrundsövertäckning som grå med 70 % opacitet:

```
.s7videoviewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Som standard visas den modala dialogrutan centrerat på skärmen på stationära datorer och tar hela webbsidans område på touchenheter. I samtliga fall hanteras placeringen och storleken på dialogrutan av komponenten. Dialogrutan styrs av följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7dialog
```

**CSS-egenskaper i dialogrutan**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Dialogrutans kantradie, om dialogrutan inte tar hela webbläsaren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Dialogrutans bakgrundsfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ska antingen vara unset eller inställd på 100 %, vilket innebär att dialogrutan tar hela webbläsarfönstret (det här läget rekommenderas på enheter med pekskärm). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Ska antingen vara unset eller inställd på 100 %, vilket innebär att dialogrutan tar hela webbläsarfönstret (det här läget rekommenderas på enheter med pekskärm). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in dialogrutan så att den använder hela webbläsarfönstret och har en vit bakgrund på pekenheter:

```
.s7videoviewer .s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Dialogrutans rubrik består av en ikon, en titeltext och en stängningsknapp. Rubrikbehållaren styrs med

```
.s7videoviewer .s7linkdialog .s7dialogheader
```

**CSS-egenskaper för dialogrutans rubrik**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p> Inre utfyllnad för rubrikinnehåll. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ikonen och rubriktexten placeras i en extra behållare som styrs med

```
.s7videoviewer .s7linkdialog .s7dialogheader .s7dialogline
```

**CSS-egenskaper för dialograden**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p> Inre utfyllnad för rubrikikonen och titeln </p> </td> 
  </tr> 
 </tbody> 
</table>

Rubrikikonen styrs med följande CSS-klassväljare

```
.s7videoviewer .s7linkdialog .s7dialogheadericon
```

**CSS-egenskaper för dialogrutans rubrikikon**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ikonens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Ikonhöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Ikonbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Rubriken styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7dialogheadertext
```

**CSS-egenskaper för rubriktexten i dialogrutan**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Teckenbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Teckenhöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsfamilj. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p>Intern textutfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Stängningsknappen styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7closebutton
```

**CSS-egenskaper för stängningsknappen **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Lodrät knappposition i förhållande till rubrikbehållare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger  </span> </p> </td> 
   <td colname="col2"> <p> Vågrät knappposition i förhållande till rubrikbehållare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Knappbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Knapphöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p>Knappens inre utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Knappbild för varje läge. </p> </td> 
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

Knappbeskrivningen Stäng och dialogrutans titel kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Exempel - Om du vill ställa in en dialogruterubrik med utfyllnad, en ikon med storleken 22 x 12 pixlar, en rubrik med 16 punkter i fet stil och en stängningsknapp med storleken 28 x 28 pixlar som placeras två pixlar uppifrån och två pixlar från höger om dialogrutan:

```
.s7videoviewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Sidfoten i dialogrutan består av knappen &quot;Avbryt&quot;. Sidfotsbehållaren styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7dialogfooter
```

**CSS-egenskaper för dialogrutans sidfot **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Kant som du kan använda för att visuellt separera sidfoten från resten av dialogrutan. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sidfoten har en inre behållare som behåller knappen. Den styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7dialogbuttoncontainer
```

**CSS-egenskaper för behållaren för dialogruteknappen**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p> Inre utfyllnad mellan sidfoten och knappen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Knappen Markera allt styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7dialogactionbutton
```

Knappen är bara tillgänglig på stationära datorer.

**CSS-egenskaper för knappen Markera alla**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Knappbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Knapphöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg  </span> </p> </td> 
   <td colname="col2"> <p> Knapptextfärg för varje läge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Knappbakgrundsfärg för varje läge. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Knappen Markera allt har stöd för attributväljaren `state`, som kan användas för att tillämpa olika skal på olika knapplägen.

Knappen Avbryt styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7dialogcancelbutton
```

**CSS-egenskaper för knappen Avbryt i dialogrutan**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Knappbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Knapphöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg  </span> </p> </td> 
   <td colname="col2"> <p> Knapptextfärg för varje läge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Knappbakgrundsfärg för varje läge. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder attributväljaren `state`, som kan användas för att tillämpa olika skal på olika knapplägen.

Dessutom har båda knapparna samma gemensamma CSS-klass som kan innehålla CSS-inställningar som är desamma för andra dialogruteknappar:

```
.s7videoviewer .s7linkdialog .s7dialogfooter .s7button
```

**CSS-egenskaper för knappen**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Knappens teckensnittsbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Knappens teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Knappteckensnittsfamilj. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p> Texthöjd inuti knappen. Påverkar lodrät justering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow  </span> </p> </td> 
   <td colname="col2"> <p>Skugga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-höger  </span> </p> </td> 
   <td colname="col2"> <p>Högerknappsmarginal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Knappverktygstipsen kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Exempel - om du vill ställa in en dialogruteslut med knappen Avbryt (64 x 34), där textfärgen och bakgrundsfärgen är olika för varje knappläge:

```
.s7videoviewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Dialogrutans huvudområde (mellan sidhuvudet och sidfoten) innehåller dialogruteinnehåll. I samtliga fall hanterar komponenten bredden på det här området - det går inte att ange den i CSS. Huvudområdet i dialogrutan styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7dialogviewarea
```

**CSS-egenskaper i dialogrutans visningsområde **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> Höjden på området i huvuddialogrutan. Den ska bara anges när dialogrutan fungerar i skrivbordsläge. Det är inte tillämpligt när dialogrutans storlek ändras så att den upptar hela webbläsarfönstret. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärgen i huvuddialogrutan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal  </span> </p> </td> 
   <td colname="col2"> <p>Yttre marginal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in ett huvudområde i dialogrutan till 300 pixlars höjd, har en marginal på tio pixlar och använder en vit bakgrund:

```
.s7videoviewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Allt formulärinnehåll (som etiketter och inmatningsfält) finns inuti en behållare som styrs med

```
.s7videoviewer .s7linkdialog .s7dialogbody
```

**CSS-egenskaper för dialogrutans brödtext **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in formulärinnehåll så att det har utfyllnad på tio pixlar:

```
.s7videoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

Alla statiska etiketter i dialogruteformuläret styrs med

```
.s7videoviewer .s7linkdialog .s7dialoglabel
```

Den här klassen är inte lämplig för att styra etikettens storlek eller placering eftersom du kan använda den på texter på olika ställen i användargränssnittet.

**CSS-egenskaper för dialogruteetiketten. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Etikettens teckensnittsbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsstorlek för etikett. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Etikettteckensnittsfamilj. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg  </span> </p> </td> 
   <td colname="col2"> <p>Textfärg för etikett. </p> </td> 
  </tr> 
 </tbody> 
</table>

Dialogruteetiketterna kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Exempel - om du vill ställa in alla etiketter till grått, fet med ett teckensnitt på nio pixlar:

```
.s7videoviewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Storleken på textkopian som visas ovanpå länken styrs av följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7dialoginputwide
```

**CSS-egenskaper för dialogrutans inmatningsfält**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Textbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ange att textkopian ska vara 430 pixlar bred och ha en utfyllnad på tio pixlar längst ned:

```
.s7videoviewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Delningslänken kapslas i en behållare och styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7dialoginputcontainer
```

**CSS-egenskaper för dialogrutans indatabehållare**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Kant runt delningslänkens behållare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ange en grå kant på en pixel runt inbäddningskoden och ha nio pixlar utfyllnad:

```
.s7videoviewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

Själva delningslänken styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7linkdialog .s7dialoglink
```

**CSS-egenskaper för länken för delning av dialogruta**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Dela länkbredd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ange delningslänken som 450 pixlar bred:

```
.s7videoviewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```

