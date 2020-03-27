---
description: Sökresultatpanelen består av sökrutan högst upp och huvudområdet där informationsmeddelanden eller sökresultat visas.
seo-description: Sökresultatpanelen består av sökrutan högst upp och huvudområdet där informationsmeddelanden eller sökresultat visas.
seo-title: Sökresultatpanel
solution: Experience Manager
title: Sökresultatpanel
topic: Dynamic media
uuid: 43d8e003-79f7-4e41-98d7-b362ab7180ea
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Sökresultatpanel{#search-results-panel}

Sökresultatpanelen består av sökrutan högst upp och huvudområdet där informationsmeddelanden eller sökresultat visas.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

När panelen är aktiv visas visningsprogrammets användargränssnitt med en halvgenomskinlig fyllning. Färgen och opaciteten för den här fyllningen styrs med följande CSS-klassväljare:

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
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
   <td colname="col2"> <p>Övertäckningens färg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacitet </span> </p> </td> 
   <td colname="col2"> <p>Färgens opacitet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sökresultatpanelen upptar alltid alla tillgängliga höjder för visningsprogrammet. Du kan dock konfigurera bredden. Du kan ange bredden till ett absolut pixelvärde, vilket är standardinställningen för brytpunkter i mellanstorlek och stor storlek. Du kan också ange bredden till 100 % så att sökresultatpanelen upptar hela visningsområdet. Panelbredden styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**CSS-egenskap för sökresultatrymden**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på sökresultatrymden. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en 250 pixlar bred sökresultatpanel på stora och medelstora brytpunkter och använda en panel i full storlek på en liten brytpunkt:

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

Den övre delen av sökresultatpanelen är dedikerad till sökrutan. Utfyllnaden på inmatningsrutans sidor styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**CSS-egenskaper för sökindatabehållaren**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p> Utfyllnad runt inmatningsrutan. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sökindatafältet styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**CSS-egenskaper för sökinmatningsfältet**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på sökinmatningsfältet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left </span> </p> </td> 
   <td colname="col2"> <p> Den inre utfyllnaden mellan inmatningsfältets gränser och inmatningstexten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Kant för sökinmatningsfältet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p>Marginal för sökinmatningsfältet </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Storlek på textteckensnittet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in ett sökinmatningsfält med 0 pixlar i höjd och 14 pixlar i teckensnitt:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

Sökknappen till vänster om sökinmatningsfältet i form av &quot;lookglass&quot; styrs som standard av följande CSS-klassväljare:

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**CSS-egenskaper för indataknappen för sökning**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på indataknappen för sökning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på indataknappen för sökning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>URL:en till ikonbilden för "lookglass". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-size </span> </p> </td> 
   <td colname="col2"> <p>Storleken på ikonen för "lookglass". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Kant på indataknappen för sökning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p>Marginal för sökknappen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in en sökknapp med 26 x 26 pixlar &quot;look glass&quot;-ikon; 30 pixlar stor med en kant på 1 pixel:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton { 
 width:30px; 
 height:30px; 
 background-size:26px 26px; 
 background-image: url(images/v2/Search_form_field.png); 
 font-size:14px; 
 border: 1px solid #696969; 
}
```

Sökresultatpanelen kan visa en textfråga när funktionen anropas för första gången. Det visar också ett meddelande för användaren när sökningen inte gav några resultat. I samtliga fall visas texten i huvuddelen av sökresultatpanelen och styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**CSS-egenskaper för sökinformationen**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p> Textens färg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Namn på textteckensnitt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>Vågrät textjustering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Storlek på teckensnittstext. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här textpanelen har stöd för attributväljaren, som kan användas för att tillämpa olika format på olika textmeddelanden. `state` motsvarar i synnerhet den textprompt som visas när panelen anropas för första gången, `state='prompt'` `state='results'` motsvarar texten med information om sökträffar, och `state='no_results'` motsvarar den text som visas när sökfrågan inte returnerade några resultat.

Meddelandetexten kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - för att ställa in en textpanel som använder ett grått teckensnitt på 18 pixlar:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

Sökresultaten återges som en enda kolumn eller som en enda rad med miniatyrbilder för sidor med sökträffar. Avståndet mellan miniatyrbilder av sökresultat styrs med följande CSS-klassväljare:

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**CSS-egenskaper för miniatyrcellerna**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p> Storleken på den lodräta marginalen runt varje miniatyrbild. Det faktiska mellanrummet för miniatyrbilder är lika med summan av de övre och nedre marginalerna som angetts för <span class="codeph"> .s7miniatyrcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in 10 pixelavstånd:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Utseendet på enskilda miniatyrbilder styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**CSS-egenskaper för miniatyrbilden**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
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

Exempel - Om du vill ställa in miniatyrbilder som är 215 x 129 pixlar har du en ljusgrå standardkantlinje och en mörkgrå markerad kantlinje:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

Utseendet på miniatyrbildetiketten styrs av följande CSS-klassväljare:

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**CSS-egenskaper för etiketten**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p> Textfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Namn på textteckensnitt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Storlek på textteckensnitt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in etiketter som använder teckensnittet 12 pixlar, grå, Helvetica:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

På system där musindata används visas två rullningsknappar längst ned på sökresultatpanelen för att användaren ska kunna bläddra igenom sökresultaten. Utseendet på upp- och nedrullningsknapparna styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

Det går inte att placera rullningsknappar med CSS-egenskaperna top, left, bottom och right. I stället placerar visningsprogramlogiken dem automatiskt.

**CSS-egenskaper för rullningsknapparna uppåt och nedåt**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
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
>Den här knappen har stöd för attributväljaren, som kan användas för att tillämpa olika skal på `state` , `"up"``"down"`och `"over"``"disabled"` knapplägen.

Knappverktygstipsen kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Exempel - för att ställa in en rullningsknapp som är 125 x 35 pixlar och har olika teckningar för varje läge:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_disabled.png);
```

