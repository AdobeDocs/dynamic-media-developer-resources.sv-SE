---
description: Färgrutor består av en rad med miniatyrbilder med valfria rullningsknappar på vänster och höger sida.
seo-description: Färgrutor består av en rad med miniatyrbilder med valfria rullningsknappar på vänster och höger sida.
seo-title: Färgrutor
solution: Experience Manager
title: Färgrutor
topic: Dynamic media
uuid: 92360088-7199-49c3-80ee-e175d234a78e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Färgrutor{#swatches}

Färgrutor består av en rad med miniatyrbilder med valfria rullningsknappar på vänster och höger sida.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Rullningsknappar visas bara på skrivbordet om alla miniatyrer inte får plats i behållarens bredd. På mobila enheter, eller om miniatyrbilder får plats i behållarbredden, visas inte rullningsknappar.

**CSS-egenskaper för färgrutorna**

Utseendet på färgrutebehållaren styrs med följande CSS-klassväljare:

```
.s7flyoutviewer .s7swatches
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på färgrutorna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på färgrutorna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p> Den lodräta färgrutans förskjutning i förhållande till visningsprogrammets behållare. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in färgrutor till 460 x 100 pixlar:

```
.s7flyoutviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

**CSS-egenskaper för mellanrum för miniatyrfärgrutor**

Avståndet mellan miniatyrbilder av färgrutor styrs med CSS-klassväljaren:

```
.s7flyoutviewer .s7swatches .s7thumbcell
```

<table id="table_70FAD50E38EB4647B8FAB832F552BBB8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
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

Exempel - för att ställa in mellanrummet så att det är 10 pixlar både lodrätt och vågrätt:

```
.s7flyoutviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

**CSS-egenskaper för miniatyrbildsfärgrutor**

Utseendet på enskilda miniatyrbilder styrs med följande CSS-klassväljare:

```
.s7flyoutviewer .s7swatches .s7thumb
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på miniatyrfärgrutorna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på miniatyrfärgrutorna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Kanten på miniatyrfärgrutorna. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniatyrbilden har stöd för attributväljaren, som används för att tillämpa olika skal på olika miniatyrlägen. `state` Motsvarar i synnerhet miniatyrbilden för den bild som visas i huvudvyn, `state="selected"` motsvarar resten av miniatyrbilderna och `state="default"` `state="over"` används vid muspekaren.

Exempel - Om du vill ställa in miniatyrbilder som är 56 x 56 pixlar har du en ljusgrå standardkant och en mörkgrå markerad kant:

```
.s7flyoutviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7flyoutviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7flyoutviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

**CSS-egenskaper för vänster och höger rullningsknapp**

Utseendet på vänster och höger rullningsknapp styrs av följande CSS-klassväljare:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton 
.s7flyoutviewer .s7swatches .s7scrollrightbutton
```

Det går inte att placera rullningsknappar med CSS- `top`, `left`och `bottom``right` -egenskaper. I stället placerar visningsprogramlogiken dem automatiskt.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på rullningsknappen. </p> </td> 
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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#section-b0af39db1af74561aea9fddcc8cdc2c7" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för attributväljaren, som används för att tillämpa olika skal på knapplägen `state` , `up`, `down`och `over``disabled`.

Knappverktygstipsen kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) .

Exempel - för att ställa in rullningsknappar som är 56 x 56 pixlar och har olika teckningar för varje läge:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```

