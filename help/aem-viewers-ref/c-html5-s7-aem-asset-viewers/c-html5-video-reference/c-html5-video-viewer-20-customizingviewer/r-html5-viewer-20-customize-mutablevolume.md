---
description: Inledningsvis visas den ändringsbara volymkontrollen som en knapp där användaren kan stänga av eller slå på ljudet i videospelaren.
seo-description: Inledningsvis visas den ändringsbara volymkontrollen som en knapp där användaren kan stänga av eller slå på ljudet i videospelaren.
seo-title: Muterbar volym
solution: Experience Manager
title: Muterbar volym
topic: Dynamic media
uuid: d7eafff8-dd98-42e2-9d45-e291fe372d8c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---


# Ändringsbar volym{#mutable-volume}

Inledningsvis visas den ändringsbara volymkontrollen som en knapp där användaren kan stänga av eller slå på ljudet i videospelaren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

När en användare rullar över knappen visas ett reglage som gör att användaren kan ställa in volymen. Den ändringsbara volymkontrollen kan storleksanpassas, skalas och placeras i förhållande till kontrollfältet som innehåller den av CSS.

Utseendet på området för den ändringsbara volymen styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7mutablevolume
```

**CSS-egenskaper för den ändringsbara volymen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Placera från den övre kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger  </span> </p> </td> 
   <td colname="col2"> <p> Placera från den högra kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på den ändringsbara volymkontrollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höjden på den ändringsbara volymkontrollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Färgen på den ändringsbara volymkontrollen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Utseendet på knappen för att stänga av/slå på styrs av följande CSS-klassväljare:

```
.s7videoviewer .s7mutablevolume .s7mutebutton
```

Du kan styra bakgrundsbilden för varje knappläge. Knappens storlek ärvs från volymkontrollens storlek.

**CSS-egenskaper för knappbilden**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder både attributväljarna `state` och `selected`, som kan användas för att tillämpa olika skal på olika knapplägen. `selected='true'` motsvarar i synnerhet läget &quot;muted&quot; och `selected='false'` motsvarar läget &quot;unmuted&quot;.

Det lodräta volymfältsområdet styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume
```

**CSS-egenskaper för det lodräta volymfältsområdet**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärgen för den lodräta volymen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Bredden på den lodräta volymen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> Höjden på den lodräta volymen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Spåret i den lodräta volymkontrollen styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**CSS-egenskaper för den lodräta volymkontrollen**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärgen för den lodräta volymkontrollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Bredden på den lodräta volymkontrollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höjden på den lodräta volymkontrollen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Den lodräta volymknappen styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**CSS-egenskaper för den lodräta volymkontrollknappen**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Lodrät volymkontroll - ratten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Bredden på den lodräta volymkontrollknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höjden på den lodräta volymkontrollknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster  </span> </p> </td> 
   <td colname="col2"> <p>Vågrät position för den lodräta volymkontrollknappen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

## Exempel {#section-e8caea0a303c425a8a637c2a47c06355}

Om du vill ställa in en ljudavstängningsknapp som är 32 x 32 pixlar och placerad 6 pixlar från överkanten och 38 pixlar från kontrollfältets högra kant. Visa olika bilder för vart och ett av de fyra olika knapplägena när de är markerade eller inte markerade.

```
.s7videoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

Följande är ett exempel på hur du kan formatera volymreglaget i den ändringsbara volymkontrollen.

```
.s7videoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```

Följande är ett exempel på hur du kan anpassa videospelaren så att ljud inaktiveras under uppspelning. Lägg till följande kod i visningsprogrammets inbäddningskod:

```
                "handlers":{ 
                    "initComplete":function() { 
                        videoViewer.getComponent("mutableVolume").setPosition(0); 
                        videoViewer.getComponent("mutableVolume").deactivate(); 
                    } 
                }
```

I kodexemplet ovan är volymnivån inställd på `0` för komponenten `mutableVolume`. Sedan inaktiveras samma komponent så att den inte kan användas av slutanvändaren.
