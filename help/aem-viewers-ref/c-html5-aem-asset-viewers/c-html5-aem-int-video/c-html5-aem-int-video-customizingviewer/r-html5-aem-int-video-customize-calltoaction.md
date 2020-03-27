---
description: Panelen Anrop till åtgärd visas när videon avslutas och alla interaktiva färgrutor som är associerade med videon visas.
seo-description: Panelen Anrop till åtgärd visas när videon avslutas och alla interaktiva färgrutor som är associerade med videon visas.
seo-title: Uppmaning
solution: Experience Manager
title: Uppmaning
topic: Dynamic media
uuid: 04a042d8-7329-4f1d-b3b9-312d620b1f29
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Uppmaning{#call-to-action}

Panelen Anrop till åtgärd visas när videon avslutas och alla interaktiva färgrutor som är associerade med videon visas.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Panelen består av ett rubrikområde som visar videotiteln, en knapp för att spela upp i det övre högra hörnet och faktiska interaktiva färgrutor som visas som ett rullningsbart rutnät. Du kan inaktivera panelen med [konfigurationsattributet callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6) .

Anropet till åtgärdspanelen tar alltid hela det tillgängliga visningsprogramområdet.

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

Följande CSS-klassväljare styr utseendet på bakgrundsfärgen i åtgärdspanelen:

```
.s7interactivevideoviewer .s7calltoaction
```

## CSS-egenskaper för bakgrundsfärgen för åtgärdspanelen {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärg för åtgärdspanelen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#example}

Så här ställer du in ett anrop till åtgärdspanelen med mörkgrå bakgrund:

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

Följande CSS-klassväljare styr utseendet på huvudet i åtgärdspanelen:

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## CSS-egenskaper för huvudet i åtgärdspanelen {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Rubrikens bakgrundsfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Huvudets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-bottom </span> </p> </td> 
   <td colname="col2"> <p>Rubrikens nedre kant. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#example-1}

Så här ställer du in en rubrik som är 70 pixlar hög, med en mörkgrå bakgrund och en något ljusare grå kant på två pixlar längs nederkanten:

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

Följande CSS-klassväljare styr utseendet på rubriktiteln i åtgärdspanelen:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## CSS-egenskaper för rubriktiteln i åtgärdspanelen:  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p> Textfärg inuti banderollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Radhöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Teckensnittsfamilj. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> textjustering </span> </p> </td> 
   <td colname="col2"> <p>Textjustering i banderollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left </span> </p> </td> 
   <td colname="col2"> <p>Utfyllnad till vänster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad höger </span> </p> </td> 
   <td colname="col2"> <p> Högerutfyllnad som ger utrymme för knappen Spela upp. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#example-2}

Så här ställer du in en videotitel med en radhöjd på 70 pixlar, en teckensnittsstorlek på 25 pixlar, vit färg och vänsterjusterad:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

Följande CSS-klassväljare styr utseendet på stängningsknappen i åtgärdspanelen:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## CSS-egenskaper för stängningsknappen i åtgärdspanelen: {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Placera längst upp i sidhuvudet, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger </span> </p> </td> 
   <td colname="col2"> <p>Placera till höger om sidhuvudet, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knappbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Knapphöjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Bild som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Placera inuti teckningsspriten, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen. `state`

## Exempel {#example-3}

för att ställa in en uppspelningsknapp som är 28 x 28 pixlar; placerad 20 pixlar från sidhuvudets övre och högra kant, visar olika bilder för vart och ett av de fyra olika knapplägena, hämtar teckningen från komponentens sprite-bild:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<!--<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>-->

Följande CSS-klassväljare styr utseendet på miniatyrrutnätet i åtgärdspanelen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## CSS-egenskaper för miniatyrrutnätsvyn i åtgärdspanelen:  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärg för miniatyrbildområdet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#example-4}

Så här ställer du in ett miniatyrområde med en mörkgrå bakgrund:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

Följande CSS-klassväljare styr utseendet på tumcellen i åtgärdspanelen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## CSS-egenskaper för miniatyrcellen i åtgärdspanelen: {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p> Storlek på den vågräta och lodräta marginalen runt varje miniatyrbild. </p> <p>Faktiskt vågrätt miniatyrmellanrum är lika med summan av vänster och höger marginaluppsättning för <span class="codeph"> .s7miniatyrcell </span>. Samma regel gäller även för lodräta avstånd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#example-5}

Så här anger du ett vågrätt mellanrum på 24 pixlar och ett lodrätt mellanrum på 18 pixlar:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

Följande CSS-klassväljare styr utseendet på miniatyrbilden i åtgärdspanelen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## CSS-egenskaper för miniatyrbilden i åtgärdspanelen: {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
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
>Miniatyrbilden har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika miniatyrlägen. `state` motsvarar i synnerhet `state="selected"` miniatyrbilden för den markerade bilden, `state="default"` motsvarar resten av miniatyrbilderna, används `state="over"` vid hovring av musen.

## Exempel {#example-6}

Så här ställer du in miniatyrbilder som är 94 x 100 pixlar:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

Följande CSS-klassväljare styr utseendet på miniatyretiketten i åtgärdspanelen:

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## CSS-egenskaper för miniatyrbildetiketten i åtgärdspanelen: {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p> Etikettens textfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> textjustering </span> </p> </td> 
   <td colname="col2"> <p>Etikettens vågräta justering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsnamn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsfamilj. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#example-7}

Om du vill ställa in etiketter som använder en vit färg ska du centrera 15 pixlar och använda teckensnittet Arial:

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

Om det finns fler miniatyrbilder än vad som får plats lodrätt i vyn återges en lodrät rullningslist på den högra sidan av miniatyrbilderna. Anropet till åtgärdspanelen återger som standard ett litet vertikalt fält utan reglage och rullningsknappar. Du kan dock anpassa fältet genom att ändra CSS-koden för visningsprogrammet.

Följande CSS-klassväljare styr utseendet på rullningslistområdet i åtgärdspanelen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## CSS-egenskaper för rullningslistområdet i åtgärdspanelen: {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredd på rullningslist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Lodrät rullningslist förskjutning från miniatyrbildernas övre del. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p>Lodrät förskjutning av rullningslisten från miniatyrbildernas nedre del. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger </span> </p> </td> 
   <td colname="col2"> <p> Vågrät förskjutning av rullningslist från miniatyrbildernas högra kant. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#example-8}

Så här ställer du in en rullningslist som är 22 pixlar bred och som inte har någon marginal uppifrån, till höger eller nedåt i miniatyrbildområdet:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

Rullningslistens spår är området mellan den övre och den nedre rullningslistens knappar. Komponenten ställer automatiskt in spårets position och höjd.

Följande CSS-klassväljare styr utseendet på rullningslistens spår i åtgärdspanelen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## CSS-egenskaper för rullningslisten {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på rullningsspårets list. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärg för spårfältet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#example-9}

Så här ställer du in ett rullningslistspår som är 22 pixlar brett och har en grå färg:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

Rullningslistens reglage rör sig lodrätt inom rullningsspårets område. Dess lodräta position styrs helt av komponentlogiken. Men tumshöjden ändras inte dynamiskt beroende på mängden innehåll.

Följande CSS-klassväljare styr utseendet på tumhöjden och andra proportioner:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## CSS-egenskaper för tumshöjden i åtgärdspanelen: {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Tummans bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjd på tummen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>Lodrät utfyllnad mellan spårets överkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p>Lodrät utfyllnad mellan spårets nederkant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Kantradie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Tummans färg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Bild som visas för ett givet tumläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tummen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på följande olika tumlägen: `state` `"up"`, `"down"`, `"over"`och `"disabled"`.

## Exempel {#example-10}

Om du vill ställa in ett reglage för rullningslisten som är 6 x 167 pixlar, har tre pixlar rundade hörn och en grå färg:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<!--<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>-->

Följande CSS-klassväljare styr utseendet på de övre och nedre rullningsknapparna:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

Det är inte möjligt att placera rullningsknappar med CSS-egenskaperna top, left, bottom eller right. visningsprogrammets logik placerar dem automatiskt. Anropet till åtgärdspanelen i det interaktiva visningsprogrammet använder inte de här knapparna i rullningslisten, och deras storlek anges till 0 pixlar i standard-CSS.

## CSS-egenskaper för de övre och nedre rullningsknapparna i åtgärdspanelen:  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Knappens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Knappens höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Bild som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Dessa knappar har stöd för attributväljaren, som kan användas för att tillämpa olika skal på följande olika tumlägen: `state` `"up"`, `"down"`, `"over"`och `"disabled"`.

Knappverktygstipsen kan lokaliseras. Se [Lokalisering av element](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)i användargränssnittet.

## Exempel {#example-11}

Inaktivera rullningsknappar genom att ange deras storlek till 0 och dölja dem:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```

