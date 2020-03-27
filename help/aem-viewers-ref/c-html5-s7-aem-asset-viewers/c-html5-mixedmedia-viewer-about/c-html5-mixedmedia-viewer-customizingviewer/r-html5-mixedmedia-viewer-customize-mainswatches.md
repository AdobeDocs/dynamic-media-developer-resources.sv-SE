---
description: Huvudfärgrutor består av en rad med miniatyrbilder med valfria rullningsknappar på vänster och höger sida. Rullningsknappar visas bara på skrivbordet om alla miniatyrer inte får plats i behållarens bredd. På mobila enheter, eller om miniatyrbilder får plats i behållarbredden, visas inte rullningsknappar.
seo-description: Huvudfärgrutor består av en rad med miniatyrbilder med valfria rullningsknappar på vänster och höger sida. Rullningsknappar visas bara på skrivbordet om alla miniatyrer inte får plats i behållarens bredd. På mobila enheter, eller om miniatyrbilder får plats i behållarbredden, visas inte rullningsknappar.
seo-title: Huvudfärgrutor
solution: Experience Manager
title: Huvudfärgrutor
topic: Dynamic media
uuid: a968372d-3d11-45d7-b17f-50ec998f5e88
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Huvudfärgrutor{#main-swatches}

Huvudfärgrutor består av en rad med miniatyrbilder med valfria rullningsknappar på vänster och höger sida. Rullningsknappar visas bara på skrivbordet om alla miniatyrer inte får plats i behållarens bredd. På mobila enheter, eller om miniatyrbilder får plats i behållarbredden, visas inte rullningsknappar.

Utseendet på färgrutebehållaren styrs med CSS-klassväljaren:

```
.s7mixedmediaviewer .s7swatches
```

**CSS-egenskaper för färgrutorna**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på färgrutorna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p>Den lodräta färgrutans förskjutning i förhållande till visningsprogrammets behållare. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in färgrutor med en höjd på 100 pixlar.

```
.s7mixedmediviewer .s7swatches { 
 height: 100px;  
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Avståndet mellan färgrutans miniatyrbilder styrs med följande CSS-klassväljare:

`.s7mixedmediaviewer .s7swatches .s7thumbcell`

<table id="table_ECE063DB98154E099FB024F66FF877D7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p> Storleken på den vågräta och lodräta marginalen runt varje miniatyrbild. Det faktiska mellanrummet för miniatyrbilder är lika med summan av vänster och höger marginaluppsättning för <span class="codeph"> .s7miniatyrcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exempel**

Om du vill ange avstånd till tio pixlar både lodrätt och vågrätt.

```
.s7mixedmediaviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Utseendet på den enskilda miniatyrbilden styrs av följande CSS-klassväljare:

`.s7mixedmediaviewer .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
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
>Miniatyrbilden har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika miniatyrlägen. `state` Motsvarar i synnerhet miniatyrbilden för den bild som visas i huvudvyn, `state="selected"` motsvarar resten av miniatyrbilderna och `state="default"` `state="over"` används vid hovring med musen.

Exempel - Om du vill ställa in miniatyrbilder som är 56 x 56 pixlar har du en ljusgrå standardkant och en mörkgrå markerad kant.

```
.s7mixedmediaviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7mixedmediaviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7mixedviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

Resurstypen visas som en ikon ovanpå miniatyrbilden och styrs med följande CSS-klassväljare:

`.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay`

<table id="table_460FC57D12CC4B52B3782F4DFAC3A194"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredden på ikonövertäckningen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på ikonövertäckningen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Övertäckningen har stöd för attributväljaren med följande `type` värden: `image` (för enstaka bilder), `swatchset` (för färgruteuppsättningar), `spinset` (för snurruppsättningar) och `video` (för enstaka videor eller adaptiva videouppsättningar).

Exempel - om du vill ställa in ikonövertäckningar för snurruppsättningar, färgruteuppsättningar och videoklipp:

```
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="swatchset"] { 
 background-image: url(images/v2/ThumbOverlaySwatchSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="spinset"] { 
 background-image: url(images/v2/ThumbOverlaySpinSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="video"] { 
 background-image: url(images/v2/ThumbOverlayVideo.png);  
}
```

Utseendet på vänster och höger rullningsknapp styrs av följande CSS-klassväljare:

`.s7mixedmediaviewer .s7swatches .s7scrollleftbutton`

`.s7mixedmediaviewer .s7swatches .s7scrollrightbutton`

Det går inte att placera rullningsknappar med CSS- `top`, `left`och `bottom``right` -egenskaper. I stället placerar visningsprogramlogiken dem automatiskt.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika knapplägen: `state` `up`, `down`, `over`och `disabled`.

Knappverktygstipsen kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) .

Exempel - för att ställa in rullningsknappar som är 56 x 56 pixlar och har olika teckningar för varje läge.

```
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```

