---
description: Inledningsvis visas den ändringsbara volymkontrollen som en knapp där användaren kan stänga av eller slå på ljudet i videospelaren.
seo-description: Inledningsvis visas den ändringsbara volymkontrollen som en knapp där användaren kan stänga av eller slå på ljudet i videospelaren.
seo-title: Muterbar volym
solution: Experience Manager
title: Muterbar volym
topic: Dynamic media
uuid: 3c3239ca-18fc-47ff-bc5d-2b50e1514e50
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Muterbar volym{#mutable-volume}

Inledningsvis visas den ändringsbara volymkontrollen som en knapp där användaren kan stänga av eller slå på ljudet i videospelaren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

När en användare rullar över knappen visas ett reglage som gör att användaren kan ställa in volymen. Den ändringsbara volymkontrollen kan storleksanpassas, skalas och placeras i förhållande till kontrollfältet som innehåller den av CSS.

Utseendet på området för den ändringsbara volymen styrs med följande CSS-klassväljare:

```
.s7interactivevideoviewer .s7mutablevolume
```

**CSS-egenskaper för den ändringsbara volymen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Placera från den övre kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger </span> </p> </td> 
   <td colname="col2"> <p> Placera från den högra kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på den ändringsbara volymkontrollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på den ändringsbara volymkontrollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Färgen på den ändringsbara volymkontrollen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Utseendet på knappen för att stänga av/slå på styrs av följande CSS-klassväljare:

```
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton
```

Du kan styra bakgrundsbilden för varje knappläge. Knappens storlek ärvs från volymkontrollens storlek.

**CSS-egenskaper för knappbilden**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen har stöd för både `state` - och `selected` attributväljare, som kan användas för att tillämpa olika skal på olika knapplägen. Motsvarar i synnerhet `selected='true'` läget &quot;muted&quot; och `selected='false'` motsvarar läget &quot;unmuted&quot;.

Det lodräta volymfältsområdet styrs med följande CSS-klassväljare:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume
```

**CSS-egenskaper för det lodräta volymfältsområdet**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärgen för den lodräta volymen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på den lodräta volymen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Höjden på den lodräta volymen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Spåret i den lodräta volymkontrollen styrs med följande CSS-klassväljare:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**CSS-egenskaper för spåret inuti lodrät volymkontroll**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärgen för den lodräta volymkontrollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredden på den lodräta volymkontrollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på den lodräta volymkontrollen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Den lodräta volymknappen styrs med följande CSS-klassväljare:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**CSS-egenskaper för den lodräta volymkontrollknappen**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Lodrät volymkontroll - ratten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredden på den lodräta volymkontrollknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på den lodräta volymkontrollknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster </span> </p> </td> 
   <td colname="col2"> <p>Vågrät position för den lodräta volymkontrollknappen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

## Exempel {#section-e8caea0a303c425a8a637c2a47c06355}

Om du vill ställa in en ljudavstängningsknapp som är 32 x 32 pixlar och placerad 6 pixlar från överkanten och 38 pixlar från kontrollfältets högra kant. Visa olika bilder för vart och ett av de fyra olika knapplägena när de är markerade eller inte markerade.

```
.s7interactivevideoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

Följande är ett exempel på hur du kan formatera volymreglaget i den ändringsbara volymkontrollen.

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```

