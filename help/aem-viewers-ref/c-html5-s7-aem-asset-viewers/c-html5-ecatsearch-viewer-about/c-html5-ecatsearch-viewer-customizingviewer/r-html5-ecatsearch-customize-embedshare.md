---
description: Verktyget Bädda in delning består av en knapp som läggs till på panelen Dela via sociala medier och den modala dialogruta som visas när verktyget aktiveras. Knappens position hanteras helt av verktyget för social delning.
seo-description: Verktyget Bädda in delning består av en knapp som läggs till på panelen Dela via sociala medier och den modala dialogruta som visas när verktyget aktiveras. Knappens position hanteras helt av verktyget för social delning.
seo-title: Bädda in resurs
solution: Experience Manager
title: Bädda in resurs
topic: Dynamic media
uuid: 73d259fe-0978-4f47-95f6-bbfcd3b7bad1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Bädda in resurs{#embed-share}

Verktyget Bädda in delning består av en knapp som läggs till på panelen Dela via sociala medier och den modala dialogruta som visas när verktyget aktiveras. Knappens position hanteras helt av verktyget för social delning.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Utseendet på knappen för att bädda in delning styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embedshare
```

**CSS-egenskaper för verktyget för inbäddningsdelning**

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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Det går att ta bort knappen från panelen för sociala medier genom att ange `display:none` CSS-egenskapen i dess CSS-klass.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - för att ställa in en knapp för inbäddningsdelning som är 28 x 28 pixlar och visar en annan bild för vart och ett av de fyra olika knapplägena:

```
.s7ecatalogsearchviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

Bakgrundsöverlägget som täcker webbsidan när dialogrutan är aktiv styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7backoverlay
```

**CSS-egenskaper för bakgrundsövertäckningen**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacitet </span> </p> </td> 
   <td colname="col2"> <p>Opacitet för bakgrundsövertäckning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsövertäckningsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en bakgrundsövertäckning som grå med 70 % opacitet:

```
.s7ecatalogsearchviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Som standard visas den modala dialogrutan centrerat på skärmen på stationära datorer och tar hela webbsidans område på touchenheter. I samtliga fall hanteras placeringen och storleken på dialogrutan av komponenten. Dialogrutan styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialog
```

**CSS-egenskaper i dialogrutan**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Dialogrutans kantradie, om dialogrutan inte tar hela webbläsaren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Dialogrutans bakgrundsfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ska antingen vara unset eller inställd på 100 %, vilket innebär att dialogrutan tar hela webbläsarfönstret (det här läget rekommenderas på enheter med pekskärm). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Ska antingen vara unset eller inställd på 100 %, vilket innebär att dialogrutan tar hela webbläsarfönstret (det här läget rekommenderas på enheter med pekskärm). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in dialogrutan så att den använder hela webbläsarfönstret och har en vit bakgrund på pekenheter:

```
.s7ecatalogsearchviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Dialogrutans rubrik består av en ikon, en titeltext och en stängningsknapp. Rubrikbehållaren styrs med

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader
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
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader .s7dialogline
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
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadericon
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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Rubriken styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadertext
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
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton
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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - för att ställa in dialoghuvud med utfyllnad, 24 x 14 pixlars ikon, fet 16 punkters titel och stängningsknapp på 28 x 28 pixlar, placerad två pixlar uppifrån och två pixlar från höger om dialogbehållare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Sidfoten i dialogrutan består av knappen &quot;Avbryt&quot;. Sidfotsbehållaren styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter
```

**CSS-egenskaper för dialogrutans sidfot **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> Kant som du kan använda för att visuellt separera sidfoten från resten av dialogrutan. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sidfoten har en inre behållare som behåller knappen. Den styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbuttoncontainer
```

**CSS-egenskaper för behållaren för dialogruteknappen**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p> Inre utfyllnad mellan sidfoten och knappen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Knappen Markera allt styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton
```

Knappen är bara tillgänglig på stationära datorer.

**CSS-egenskaper för knappen Markera alla**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
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
>Knappen Markera allt har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Knappen Avbryt styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton
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

Dessutom har båda knapparna samma gemensamma CSS-klass som kan innehålla CSS-inställningar som är desamma för andra dialogruteknappar:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter .s7button
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

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - om du vill ställa in en dialogruteslut med en Avbryt-knapp på 64 x 34, en Markera alla-knapp på 82 x 34 och ha en textfärg och bakgrundsfärg som skiljer sig åt för varje knappläge:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Huvuddialogrutan (mellan sidhuvudet och sidfoten) innehåller rullningsbart dialogruteinnehåll och rullningspanelen till höger. I samtliga fall hanterar komponenten bredden på det här området, det går inte att ange den i CSS. Huvudområdet i dialogrutan styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogviewarea
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

Exempel - om du vill ställa in ett huvudområde i dialogrutan till 300 pixlars höjd, har en marginal på tio pixlar och använder en vit bakgrund:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Allt formulärinnehåll (som etiketter och inmatningsfält) finns i en behållare som styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbody
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
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Alla statiska etiketter i dialogruteformuläret styrs med

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoglabel
```

Den här klassen är inte lämplig för att styra etikettens storlek eller placering eftersom du kan använda den på texter på olika ställen i användargränssnittet.

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

Dialogruteetiketter kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - om du vill ställa in alla etiketter till grått, fet med ett teckensnitt på nio pixlar:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Storleken på textkopian som visas ovanpå inbäddningskoden styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputwide
```

**CSS-egenskaper för dialogrutans inmatningsfält**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på indatafält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ange att textkopian ska vara 430 pixlar bred och ha en utfyllnad på tio pixlar längst ned:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Inbäddningskoden kapslas i behållaren och styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer
```

**CSS-egenskaper för dialogrutans indatabehållare**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredden på behållaren för inbäddningskoden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Kant runt behållaren för inbäddningskoden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ange en grå kant på en pixel runt inbäddad kodtext, gör den 430 pixlar bred och har en utfyllnad på tio pixlar:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

Den faktiska inbäddningskodtexten styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer
```

**CSS-egenskaper för dialogrutans indatabehållare**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap </span> </p> </td> 
   <td colname="col2"> <p>Radbrytningsformat. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in inbäddningskod så att `break-word` automatisk radbrytning används:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

Etiketten och listrutan för inbäddningsstorlek finns längst ned i dialogrutan och placeras i en behållare som styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS-egenskaper för panelen Bädda in storlek i dialogrutan**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in en panel för inbäddningsstorlek så att den har tio pixlar utfyllnad:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

Storleken och justeringen för etiketten för inbäddningsstorlek styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS-egenskaper för panelen Bädda in storlek i dialogrutan**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> lodrät justering </span> </p> </td> 
   <td colname="col2"> <p>Lodrät etikettjustering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Etikettens bredd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ange att etiketten för inbäddningsstorlek ska vara justerad uppåt och 80 pixlar bred:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

Bredden på kombinationsrutan för inbäddningsstorlek styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox
```

**CSS-egenskaper för kombinationsrutan**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på kombinationsruta. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Kombinationsrutan har stöd för attributväljaren med möjliga värden för `expanded` och `true` `false`. `true` används när kombinationsrutan visar en fördefinierad inbäddningsstorlek, vilket innebär att all tillgänglig bredd används. `false` används när alternativet för anpassad storlek är markerat i kombinationsrutan, så det bör krympa för att ge utrymme för anpassade indatafält för bredd och höjd.

Exempel - Att ställa in kombinationsrutan för inbäddningsstorlek till 300 pixlar bred när ett fördefinierat objekt visas och 110 pixlar bred när en anpassad storlek visas:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

Höjden på kombinationsrutetexten definieras av ett särskilt inre element och styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**CSS-egenskaper för kombinationsrutetexten**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Texthöjd för kombinationsruta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in kombinationsrutans inbäddningsstorlek på 40 pixlar:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

Kombinationsrutan har en nedrullningsknapp till höger och den styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**CSS-egenskaper för kombinationsruteknappen**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Lodrät knappposition inuti kombinationsrutan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger </span> </p> </td> 
   <td colname="col2"> <p>Vågrät knappposition inuti kombinationsrutan. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Knappbild för varje läge. </p> </td> 
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

Exempel - om du vill ställa in en nedrullningsknapp på 28 x 28 pixlar och ha en separat bild för varje läge:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

Panelen med listan över inbäddningsstorlekar som visas när kombinationsrutan öppnas styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7comboboxdropdown
```

Panelens storlek och position styrs av komponenten. Det går inte att ändra den med CSS.

**CSS-egenskaper för kombinationsrutans listruta**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Panelkant. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ange att kombinationsrutepanelen ska ha en grå kant på en pixel:

```
.s7ecatalogsearchviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Ett enskilt objekt i en nedrullningsbar panel som styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dropdownitemanchor
```

**CSS-egenskaper för det nedrullningsbara objektets ankarpunkt**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Objektbakgrund. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ange att objektet i kombinationsrutepanelen ska ha en vit bakgrund:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

En bock visas till vänster om det markerade objektet i kombinationsrutepanelen som styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7checkmark
```

**CSS-egenskaper för kryssrutan**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
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
   <td colname="col2"> <p>Objektbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ange bockmarkeringsikonen till 25 x 25 pixlar:

```
.s7ecatalogsearchviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

När alternativet Anpassad storlek är markerat i kombinationsrutan för inbäddningsstorlek visas två extra inmatningsfält till höger så att användaren kan ange en anpassad inbäddningsstorlek. Dessa fält placeras i en behållare som styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsizepanel
```

**CSS-egenskaper för den anpassade storlekspanelen i dialogrutan**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster </span> </p> </td> 
   <td colname="col2"> <p> Avstånd från kombinationsrutan för inbäddningsstorlek. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill att fältpanelen för anpassade indatastorlekar ska vara 20 pixlar till höger om kombinationsrutan:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Varje indatafält med anpassad storlek kapslas i en behållare som återger en kant och anger marginalen mellan fälten. Den styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsize
```

**CSS-egenskaper för dialogrutans anpassade storlek**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Kant runt inmatningsfältet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredd på indatafält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p> Indatafältsmarginal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p> Utfyllnad för indatafält. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ange att indatafälten med anpassad storlek ska ha en grå kant, marginal, utfyllnad på en pixel och vara 70 pixlar bred:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Om du behöver rulla lodrätt återges rullningslisten i panelen nära den högra kanten av dialogrutan, som styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogscrollpanel
```

**CSS-egenskaper för dialogrutans rullningspanel**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på rullningspanelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in en rullningspanel så att den är 44 pixlar bred

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

Utseendet på rullningslistområdet styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar
```

**CSS-egenskaper för rullningslisten**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på rullningslist. </p> </td> 
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

Exempel - för att ställa in en rullningslist som är 28 pixlar bred och har en åtta pixelmarginaler uppifrån, till höger och nedåt på rullningspanelen:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Rullningslistens spår är området mellan den övre och den nedre rullningsknappen. Komponenten ställer automatiskt in spårets position och höjd. Spåret styrs med följande CSS-klassväljare

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**CSS-egenskaper för rullningslistens spår**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Spårbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Spåra bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in ett rullningslistspår som är 28 pixlar brett och har en grå bakgrund:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Rullningslistens reglage rör sig lodrätt inom ett rullningsspårsområde. Dess lodräta position styrs helt av komponentlogiken. Höjden på tummen ändras dock inte dynamiskt beroende på mängden innehåll. Miniatyrhöjden och andra aspekter kan konfigureras med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**CSS-egenskaper för rullningslistens reglage**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Miniatyrbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjd på tummen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>Den lodräta utfyllnaden mellan spårets överkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> Den lodräta utfyllnaden mellan spårets nederkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst tumläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tummen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika tumlägen: `state` `up`, `down`, `over`och `disabled`.

Exempel - om du vill ställa in en rullningslist som är 28 x 45 pixlar, har en marginal på tio pixlar över och under och har olika teckningar för varje läge:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

Utseendet på de övre och nedre rullningsknapparna styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Det går inte att placera rullningsknappar med CSS- `top`, `left`och `bottom``right` -egenskaper. I stället placerar visningsprogramlogiken dem automatiskt.

**CSS-egenskaper för de övre och nedre rullningsknapparna**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Dessa knappar har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen: `state` `up`, `down`, `over`och `disabled`.

Knappverktygstipsen kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - för att ställa in rullningsknappar som är 28 x 32 pixlar och har olika teckningar för varje läge:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

