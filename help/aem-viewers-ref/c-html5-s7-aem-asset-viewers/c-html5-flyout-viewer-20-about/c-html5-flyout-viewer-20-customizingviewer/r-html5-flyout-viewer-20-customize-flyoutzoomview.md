---
description: Huvudvyn består av den statiska bilden, den zoomade bilden som visas i den utfällbara vyn, det markeringsnavigeringsområde som visas över den statiska bilden och det tips som visas ovanpå den statiska bilden.
seo-description: Huvudvyn består av den statiska bilden, den zoomade bilden som visas i den utfällbara vyn, det markeringsnavigeringsområde som visas över den statiska bilden och det tips som visas ovanpå den statiska bilden.
seo-title: Utfällbar zoomvy
solution: Experience Manager
title: Utfällbar zoomvy
topic: Dynamic media
uuid: 35c60228-3044-442b-a8e2-e13d0bd306a5
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Utfällbar zoomvy{#flyout-zoom-view}

Huvudvyn består av den statiska bilden, den zoomade bilden som visas i den utfällbara vyn, det markeringsnavigeringsområde som visas över den statiska bilden och det tips som visas ovanpå den statiska bilden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Om dimensionerna för den bild som visas inte matchar dimensionerna för den utfällbara zoomvyn centreras bildinnehållet i den utfällbara zoomvyns rektangulära visningsområde.

**CSS-egenskaper för huvudvyn**

Utseendet på huvudvyn styrs med följande CSS-klassväljare:

```
.s7flyoutviewer .s7flyoutzoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Huvudvyns bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att göra huvudvyn genomskinlig:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**CSS-egenskaper för den utfällbara vyn**

Utseendet på den utfällbara vyn styrs av följande CSS-klassväljare:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster </span> </p> </td> 
   <td colname="col2"> <p> Den utfällbara vyns vågräta position i förhållande till huvudvyns övre vänstra hörn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Den utfällbara vyns lodräta position i förhållande till huvudvyns övre vänstra hörn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på den utfällbara vyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på den utfällbara vyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Den utfällbara vyns kantlinje. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en utfällbar vy till 600 x 400 pixlar, som visas med 100 pixlar förskjuten till höger om huvudvyn 512 x 288 som visas i föregående exempel:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**CSS-egenskaper för högdagern i huvudvyn**

Utseendet på högdagern i huvudvyn styrs av följande CSS-klassväljare:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

Det går att styra attribut för bakgrund, kant, genomskinlighet och liknande med hjälp av CSS. Storleken och positionen för DOM-elementet för högdager hanteras emellertid av visningslogiken. Det går inte att åsidosätta den via CSS.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Färgen på högdagern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacitet </span> </p> </td> 
   <td colname="col2"> <p> Högdageropacitet. </p> <p>I Internet Explorer 8 använder du <span class="codeph"> filter:alpha(opacity-...) ); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Kantmarkeringen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in grön högdager med 40 % genomskinlighet och en röd kant på en pixel:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**CSS-egenskaper för markören**

När `highlightmode` parametern är inställd på `cursor`ersätts markeringen i huvudvyn med en markörteckning i fast storlek, som styrs med CSS-klassväljaren:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

Det går att styra bakgrundsbilden och storleken med CSS.

Tillämpliga CSS-egenskaper är:

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Markörgrafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Markörbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Markörhöjd. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Markören har stöd för attributväljaren, som kan användas för att använda olika markörteckningar och storlekar för olika enheter. `input` motsvarar i synnerhet datorsystemen och `input="mouse"` `input="touch"` motsvarar touchenheterna.

**CSS-egenskaper för övertäckningen**

När `overlay` parametern är inställd på `1`styrs området runt markeringsramen eller markörbilden med CSS-klassväljaren:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Övertäckningsfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacitet </span> </p> </td> 
   <td colname="col2"> <p>Övertäckningsopacitet. </p> </td> 
  </tr> 
 </tbody> 
</table>

**CSS-egenskaper för tipsmeddelandet**

Utseendet på tipsmeddelandet styrs av följande CSS-klassväljare:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

Det går att konfigurera teckensnittsstil, storlek och lodrät förskjutning via CSS. Den vågräta justeringen hanteras emellertid av visningsprogrammets logik. Det går inte att åsidosätta den via CSS med `left` eller `right` .

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p>Förskjutning längst ned i huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Textfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsnamn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Utfyllnad runt meddelandetexten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfyllningsfärg för meddelandetext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Meddelandetextens kantradie i bakgrunden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacitet </span> </p> </td> 
   <td colname="col2"> <p>Meddelandetextens bakgrundsopacitet. </p> <p>I Internet Explorer 8 använder du <span class="codeph"> filter:alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Tipsmeddelandet kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) .

Exempel - om du vill ställa in ett halvgenomskinligt tips med vitt Arial 12px-teckensnitt, förskjuts 50 pixlar från huvudvyns nederkant, utfyllnad och en rundad kant:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```

