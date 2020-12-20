---
description: Utskriftsverktyget består av en knapp som läggs till i kontrollfältet och den modala dialogruta som visas när verktyget aktiveras.
seo-description: Utskriftsverktyget består av en knapp som läggs till i kontrollfältet och den modala dialogruta som visas när verktyget aktiveras.
seo-title: Skriv ut
solution: Experience Manager
title: Skriv ut
topic: Dynamic media
uuid: 7be047d8-d1be-4bda-90ca-6b55c749cc64
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1493'
ht-degree: 0%

---


# Skriv ut{#print}

Utskriftsverktyget består av en knapp som läggs till i kontrollfältet och den modala dialogruta som visas när verktyget aktiveras.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Utseendet på utskriftsknappen styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7print
```

**CSS-egenskaper för knappen Skriv ut**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-top  </span> </p> </td> 
   <td colname="col2"> <p> Förskjutningen från kontrollfältets överkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-vänster  </span> </p> </td> 
   <td colname="col2"> <p> Avståndet till nästa knapp till vänster eller till vänster om kontrollfältet om det är den första knappen på en rad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knappens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Knappens höjd. </p> </td> 
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

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exempel - Om du vill ställa in en utskriftsknapp som är 28 x 28 pixlar och visar en annan bild för vart och ett av de fyra olika knapplägena.

```
.s7ecatalogsearchviewer .s7print { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7print[state='up'] { 
background-image:url(images/v2/Print_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7print[state='over'] { 
background-image:url(images/v2/Print_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7print[state='down'] { 
background-image:url(images/v2/Print_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7print[state='disabled'] { 
background-image:url(images/v2/Print_dark_disabled.png); 
}
```

Bakgrundsöverlägget som täcker webbsidan när dialogrutan är aktiv styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
```

**CSS-egenskaper för bakåtövertäckningen**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacitet  </span> </p> </td> 
   <td colname="col2"> <p> Opacitet för bakgrundsövertäckning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsövertäckningsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in bakgrundsövertäckningen till grått med 70 % opacitet:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Som standard visas den modala dialogrutan centrerat på skärmen på datorsystem. Dialogrutans placering och storlek hanteras av komponenten Dialogrutan styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

**CSS-egenskaper i dialogrutan**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Dialogrutans kantradie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Dialogrutans bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in en dialogruta så att den har en grå bakgrund:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

Dialogrutans rubrik består av en ikon, en titeltext och en stängningsknapp. Rubrikbehållaren styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
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

Ikonen och rubriktexten placeras i en extra behållare som styrs med följande:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
```

**CSS-egenskaper för dialograden**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p> Inre utfyllnad för rubrikikonen och titeln. </p> </td> 
  </tr> 
 </tbody> 
</table>

Rubrikikonen styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Rubriken styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
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
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder attributväljaren `state`, som kan användas för att tillämpa olika skal på olika knapplägen.

Knappbeskrivningen Stäng och dialogrutans titel kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exempel - för att ställa in dialoghuvud med utfyllnad, 22 x 22 pixlars ikon, fet 16 punkters titel och en 28 x 28 pixlars stängningsknapp placerade två pixlar uppifrån och två pixlar från höger om dialogrutans behållare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgprint_cap.png"); 
    height: 22px; 
    width: 22px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Dialogrutans sidfot består av knapparna Avbryt och Skicka till utskrift. Sidfotsbehållaren styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
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

Sidfoten har en inre behållare som behåller båda knapparna. Den styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
```

**CSS-egenskaper för behållaren för dialogruteknappen**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p> Inre utfyllnad mellan sidfoten och knapparna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Knappen Avbryt styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
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

Knappen Skicka till utskrift styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
```

**CSS-egenskaper för dialogrutans åtgärdsknapp**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
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

Knappverktygstipsen kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exempel - om du vill ställa in en dialogruteslut med knappen Avbryt 64 x 34 och knappen Skicka till utskrift 96 x 34, med textfärgen och bakgrundsfärgen olika för varje knappläge:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton { 
 width:96px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Dialogrutans huvudområde (mellan sidhuvudet och sidfoten) innehåller dialogruteinnehåll. I samtliga fall hanterar komponenten bredden på det här området, det går inte att ange den i CSS. Huvudområdet i dialogrutan styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

**CSS-egenskaper i dialogrutans visningsområde **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> Höjden på området i huvuddialogrutan. </p> </td> 
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

Exempel - om du vill ställa in ett huvuddialogruteområde så att höjden beräknas automatiskt, har en marginal på tio pixlar och använder en vit bakgrund:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

Allt formulärinnehåll (som etiketter och inmatningsfält) finns i en behållare som styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

Dialogruteformuläret fylls i rad för rad, där varje rad innehåller en del av formulärinnehållet (som en etikett och ett textinmatningsfält). En formulärrad styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**CSS-egenskaper för dialograden**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p>Utfyllnad för inre linje. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in ett dialogruteformulär så att det får tio pixlar för varje rad:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

Storleken på blocket med dialoginnehåll styrs med följande CSS-klassväljare:

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

**CSS-egenskaper för dialogrutans indatabredd**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Blockbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p>Utfyllnad för inre linje. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ange ett innehållsblock som är 430 pixlar brett och har 10 pixlar utfyllnad längst ned:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Alla statiska etiketter i dialogrutan styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
```

Den här klassen är inte lämplig för att styra etikettens storlek eller placering eftersom du kan använda den på texter på olika ställen i formuläranvändargränssnittet.

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

Dialogruteetiketter kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exempel - om du vill ställa in alla etiketter till grått, fetstil med ett teckensnitt på nio pixlar:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Indatakontrollerna placeras i behållaren och styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

**CSS-egenskaper för dialogrutans indatabehållare**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left  </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ange en utfyllnad på 30 pixlar från dialogrutans vänstra kant.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

Alternativknappar och deras bildtext styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

**CSS-egenskaper för dialogrutealternativet**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Den totala bredden på alternativknappen med en bildtext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg  </span> </p> </td> 
   <td colname="col2"> <p>Textfärg för bildtext. </p> </td> 
  </tr> 
 </tbody> 
</table>

Avståndet mellan alternativknappen och bildtexten styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

**CSS-egenskaper för indata från dialogrutealternativ**

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-höger  </span> </p> </td> 
   <td colname="col2"> <p> Avstånd mellan alternativknappen och bildtexten. </p> </td> 
  </tr> 
 </tbody> 
</table>

Numeriska väljare för val av utskriftsintervall styrs med följande CSS-klassväljare

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

**CSS-egenskaper för dialogrutans utskriftsområde**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Den numeriska väljarens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal  </span> </p> </td> 
   <td colname="col2"> <p> Avstånd runt den numeriska väljaren. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - Om du vill ställa in alla alternativknappar så att de är 150 pixlar breda med svart text, tio pixelmellanrum och 42 pixlar breda numeriska väljare:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption { 
    color: #000000; 
    width: 150px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption input { 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange { 
    margin-left: 10px; 
    margin-right: 10px; 
    width: 42px; 
}
```

Den vågräta avgränsaren mellan sidintervallmarkeringen och utskriftslayoutavsnitten styrs med följande CSS-klassväljare:

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**CSS-egenskaper för den vågräta avgränsaren**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Kant runt avgränsare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad  </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Delningsbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal  </span> </p> </td> 
   <td colname="col2"> <p>Yttre marginal </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en 430 pixlar bred gråskala med en lodrät utfyllnad på 10 pixlar på båda sidorna och en marginal på 10 pixlar längst upp:

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```

