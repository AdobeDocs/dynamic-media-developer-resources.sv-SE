---
description: Panelen för interaktiva färgrutor visas bredvid videoinnehållet om interaktiva data skickades till användaren i konfigurationen. Den består av en banderoll längst upp som återger text, till exempel"Klicka för att visa", en kolumn med en eller flera interaktiva färgrutor och två rullningsknappar (endast tillgängligt på datorer).
seo-description: Panelen för interaktiva färgrutor visas bredvid videoinnehållet om interaktiva data skickades till användaren i konfigurationen. Den består av en banderoll längst upp som återger text, till exempel"Klicka för att visa", en kolumn med en eller flera interaktiva färgrutor och två rullningsknappar (endast tillgängligt på datorer).
seo-title: Interaktiva färgrutor
solution: Experience Manager
title: Interaktiva färgrutor
topic: Dynamic media
uuid: 9f9df764-3dd0-414e-a0db-4287f0019313
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Interaktiva färgrutor{#interactive-swatches}

Panelen för interaktiva färgrutor visas bredvid videoinnehållet om interaktiva data skickades till användaren i konfigurationen. Den består av en banderoll längst upp som återger text, till exempel&quot;Klicka för att visa&quot;, en kolumn med en eller flera interaktiva färgrutor och två rullningsknappar (endast tillgängligt på datorer).

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

På datorer och pekenheter återges interaktiva färgrutor lodrätt till höger om videoinnehållet i liggande orientering. På touchenheter med stående orientering visas de längst ned i visningsprogrammet som en vågrät rad med färgrutor.

Följande CSS-klassväljare styr platsen och orienteringen för den interaktiva färgrutepanelen:

```
.s7interactivevideoviewer .s7interactiveswatches
```

## CSS-egenskaper för de interaktiva färgrutorna {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på den interaktiva färgrutepanelen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på den interaktiva färgrutepanelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Den översta positionen för den interaktiva färgrutepanelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p>Nedre position för panelen för interaktiva färgrutor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster </span> </p> </td> 
   <td colname="col2"> <p>Den vänstra positionen för den interaktiva färgrutepanelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger </span> </p> </td> 
   <td colname="col2"> <p>Den högra positionen för den interaktiva färgrutepanelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Körningsplatsen och orienteringen för den interaktiva färgrutepanelen definieras av en kombination av ovanstående CSS-egenskaper enligt följande:

* Om du vill återge interaktiva färgrutor vågrätt längst ned i visningsprogrammet anger du höjden till ett absolut pixelvärde. vänster och nerifrån till 0px; width, right, and top to auto.
* Om du vill återge interaktiva färgrutor lodrätt till höger om videoinnehållet anger du bredden till en absolut pixel. höger och uppifrån till 0px; höjd, vänster och nederst till auto.

Det går att använda CSS-markörer tillsammans med den här formateringen för att få en adaptiv placering av den interaktiva färgrutepanelen.

## Exempel {#example}

Så här ställer du in en interaktiv färgrutepanel så att den återges vågrätt längst ned i visningsprogrammet på pekenheter med liggande orientering och så att den visas lodrätt till höger om videoinnehållet i alla andra fall:

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Banderollens storlek och position hanteras av den interaktiva färgrutekomponenten baserat på andra format som används med CSS och kan inte anges explicit.

Följande CSS-klassväljare styr utseendet på banderollpanelen:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## CSS-egenskaper för banderollpanelen {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärg på banderollpanelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Textfärg i banderollpanelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Kant runt banderollpanelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Den teckensnittsvikt som ska användas för texten i banderollpanelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Den teckenstorlek som ska användas för texten i banderollpanelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Den teckensnittsfamilj som ska användas för texten i banderollpanelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>Den teckensnittsjustering som ska användas för texten i banderollpanelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Banderollverktygstipset kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

## Exempel {#section-e8caea0a303c425a8a637c2a47c06355}

Så här ställer du in en banderoll med mörkgrå bakgrund, en ljusgrå kant på två pixlar och den vita texten centrerad vågrätt:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

Följande CSS-klassväljare styr utseendet på färgrutorna:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## CSS-egenskaper för färgruteområdet {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärg för färgruteområdet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-9cadd62a09fd44a280f55ff42437e416}

Så här ställer du in färgruteområdet med mörkgrå bakgrund:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

Följande CSS-klassväljare styr mellanrummet mellan miniatyrbilder av färgrutor:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## CSS-egenskaper för färgrutornas miniatyrmellanrum {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p> Storleken på den vågräta och lodräta marginalen runt varje miniatyrbild. Det faktiska mellanrummet för miniatyrbilder är lika med summan av vänster och höger marginaluppsättning för <span class="codeph"> .s7miniatyrcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-39fb270b7e494a9d99e6e8f6890ec53c}

Så här anger du ett lodrätt avstånd på 10 pixlar:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Följande CSS-klassväljare styr utseendet på enskilda miniatyrbilder:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## CSS-egenskaper för utseendet på enskilda miniatyrbilder {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Miniatyrens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på miniatyrbilden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Miniatyrens kantlinje. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniatyrbilden har stöd för attributväljaren, som du kan använda för att använda olika skal för olika miniatyrlägen. `state` motsvarar i synnerhet `state="selected"` miniatyrbilden för den markerade bilden, `state="default"` motsvarar resten av miniatyrbilderna, används `state="over"` vid hovring av musen.

## Exempel {#section-69fec189ffaa440b97b6b846c320b75b}

Så här ställer du in miniatyrbilder som är 100 x 75 pixlar:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

Följande CSS-klassväljare styr utseendet på miniatyrbildetiketten:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## CSS-egenskaper för miniatyretikettens utseende {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Textfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Etikettkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> textjustering </span> </p> </td> 
   <td colname="col2"> <p>Vågrät textjustering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsnamn. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-eb141eb6c1154183baa69796edb90536}

Så här ställer du in etiketter som ska använda vänsterjusterad, vit, 12 pixlar i teckensnittet Helvetica och en nederkantsram:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

Följande CSS-klassväljare styr utseendet på upp- och nedrullningsknapparna:

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

Det är inte möjligt att placera rullningsknapparna med CSS- `top`, `left`och `bottom``right` egenskaper. i stället placerar visningsprogramlogiken dem automatiskt.

## CSS-egenskaper för uppåt- och nedrullningsknapparnas utseende {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på rullningsknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på rullningsknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Positionen inuti teckningsspriten, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som du kan använda för att tillämpa olika skal på knapplägena: `state` &quot; `up`&quot;, &quot; `down`&quot;, &quot; `over`&quot; och &quot; `disabled`&quot;.

Knappverktygstipsen kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

## Exempel {#section-e6ce4fa084b84288bc7583342b2c510c}

Om du vill ställa in en rullningsknapp som är 60 x 36 pixlar har du olika teckningar för varje läge och tar den teckningen från komponentens sprite-bild:

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```

