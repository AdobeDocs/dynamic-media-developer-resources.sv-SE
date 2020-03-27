---
description: Innehållsförteckningen är en knapp som finns i huvudkontrollfältet. När den är aktiverad visas en nedrullningsbar panel med en lista över sidindex och etiketter.
seo-description: Innehållsförteckningen är en knapp som finns i huvudkontrollfältet. När den är aktiverad visas en nedrullningsbar panel med en lista över sidindex och etiketter.
seo-title: Innehållsförteckning
solution: Experience Manager
title: Innehållsförteckning
topic: Dynamic media
uuid: e5da89b4-fd3f-41ab-bc55-d43c2999d4b7
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Innehållsförteckning{#table-of-contents}

Innehållsförteckningen är en knapp som finns i huvudkontrollfältet. När den är aktiverad visas en nedrullningsbar panel med en lista över sidindex och etiketter.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Baserat på konfigurationen kan listan innehålla alla sidor som finns i katalogen eller endast de sidor som har explicit definierade etiketter. Om listan är längre än de tillgängliga skärmutrymmena visas en rullningslist till höger i datorsystem.

Placeringen och storleken på innehållsförteckningsknappen i visningsprogrammets användargränssnitt styrs med följande CSS-klassväljare:

```
.s7ecatalogviewer .s7tableofcontents
```

**CSS-egenskaper för innehållsförteckningen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-top </span> </p> </td> 
   <td colname="col2"> <p> Förskjutningen från kontrollfältets överkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-vänster </span> </p> </td> 
   <td colname="col2"> <p> Avståndet till nästa knapp till vänster eller till vänster om kontrollfältet om det är den första knappen på en rad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på innehållsförteckningsknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Höjden på innehållsförteckningsknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - ställ in en innehållsförteckningsknapp som är placerad 4 pixlar från nederkanten och 43 pixlar från vänster om huvudkontrollfältet. storleken är 28 x 28 pixlar och en bild visas för vart och ett av de fyra olika knapplägena:

```
.s7ecatalogviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

Utseendet på den nedrullningsbara panelen styrs av följande CSS-klassväljare:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel
```

**CSS-egenskaper för den nedrullningsbara panelen**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärg i den nedrullningsbara panelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p> Intern förskjutning mellan panelgränserna och innehållet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p> Skugga runt panelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Det går inte att styra storleken eller placeringen av den nedrullningsbara panelen från CSS. komponenten hanterar sin layout programmatiskt.

Exempel - ställ in en nedrullningsbar panel som har en halvgenomskinlig svart bakgrund, en marginal på 5 pixlar runt innehållet och en skugga:

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

Det enskilda objektets utseende och känsla styrs med följande CSS-klassväljare:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

**CSS-egenskaper för objektet**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsnamn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Objektets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Intern utfyllnad. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Listruteobjektet har stöd för attributväljaren, som kan användas för att tillämpa olika skal för hovring och valda objektlägen. `state`

Exempel - ställ in ett nedrullningsbart objekt med Helvetica 14 pixlar och 19 pixlar högt. Ett objekt har en mörkgrå bakgrund på hovring och en ljusgrå bakgrund när det är markerat:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

Ett element som visar sidindexet styrs med följande CSS-klassväljare:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index
```

**CSS-egenskaper för sidindexet**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width </span> </p> </td> 
   <td colname="col2"> <p> Minsta elementbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p> Maximal elementbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad höger </span> </p> </td> 
   <td colname="col2"> <p> Avstånd mellan sidindexet och sidetiketten. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Du kan dölja sidindexet helt genom att ange `display:none` det för `s7index` CSS-klassen.

Exempel 1 - ställ in ett sidindex med en minsta bredd på 40 pixlar, en maximal bredd på 70 pixlar och en marginal på 5 pixlar till höger:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

Exempel 2 - dölj sidindex:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

Sideetiketten styrs med följande CSS-klassväljare:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7label
```

**CSS-egenskaper för sidetiketten**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width </span> </p> </td> 
   <td colname="col2"> <p> Minsta elementbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p> Maximal elementbredd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ställ in ett sidindex med en minsta bredd på 40 pixlar och en maximal bredd på 240 pixlar:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

Om det finns fler objekt än vad som får plats lodrätt i den nedrullningsbara panelen och systemet är ett skrivbord, återges en lodrät rullningslist till höger på panelen. Utseendet på rullningslistområdet styrs med följande CSS-klassväljare:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

**CSS-egenskaper för rullningslisten**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på rullningslisten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Den lodräta rullningslistens förskjutning från panelområdets överkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p> Den lodräta rullningslistens förskjutning från panelområdets nederkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger </span> </p> </td> 
   <td colname="col2"> <p> Den vågräta rullningslistens förskjutning från panelområdets högra kant. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ställ in en rullningslist som är 28 pixlar bred och som inte har någon marginal för panelens övre, högra eller nedre del:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

Rullningslistens spår är området mellan den övre och den nedre rullningsknappen. Komponenten ställer automatiskt in spårets position och höjd. Spåret styrs med följande CSS-klassväljare:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**CSS-egenskaper för rullningsspåret**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
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

Exempel - ställ in ett rullningslistspår som är 28 pixlar brett och har en halvgenomskinlig grå bakgrund:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Rullningslistens reglage rör sig lodrätt inom rullningsspårets område. Dess lodräta position styrs av komponentlogiken. Höjden på tummen ändras dock inte dynamiskt beroende på mängden innehåll. Du kan konfigurera tumhöjden och andra aspekter med följande CSS-klassväljare:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**CSS-egenskaper för rullningslistens reglage**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
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
   <td colname="col2"> <p>Den lodräta utfyllnaden mellan spårets nederkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett givet tumläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tummen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på lägena `state` , `up`, `down`och `over``disabled` tummen.

Exempel - Ställ in en rullningslist som är 28 x 45 pixlar, har 10 pixelmarginaler högst upp och längst ned och har olika teckningar för varje läge:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

Utseendet på de övre och nedre rullningsknapparna styrs av följande CSS-klassväljare:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

Det är inte möjligt att placera rullningsknapparna med CSS- `top`, `left`och `bottom``right` egenskaper. i stället placerar visningsprogramlogiken dem automatiskt.

**CSS-egenskaper för knappen för rullning uppåt och nedåt**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på lägena `state` , `up`, `down`och `over``disabled` button.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - ställ in rullningsknappar som är 28 x 32 pixlar och har olika teckningar för varje läge:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```

