---
title: Videoskrubber
description: Videonavigeringen är den vågräta skjutreglaget som gör att en användare dynamiskt kan söka till valfri tidsposition i den video som spelas upp
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 404e39d4-565e-4dde-b2bd-fa83a895d001
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 0%

---

# Videoskrubber{#video-scrubber}

Videonavigeringen är den vågräta skjutreglaget som gör att en användare dynamiskt kan söka till valfri tidsposition i den video som spelas upp.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Rubbens &#39;knob&#39; rör sig också när videon spelas upp för att ange videons aktuella tidsposition under uppspelningen. Videonavigeringslisten har alltid hela kontrollfältets bredd. Det går att skapa skal för videospolaren och ändra dess höjd och lodräta position med CSS.

Videonavigeringens allmänna utseende styrs med följande CSS-klassväljare:

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**CSS-egenskaper för videonavigeringsprogrammet**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> övre </span> </p> </td> 
   <td colname="col2"> <p>Placera från den övre kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p> Placera från den nedre kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på videobandspelaren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Färgen på videobandspelaren. </p> </td> 
  </tr> 
 </tbody> 
</table>

Följande CSS-klassväljare spårar indikatorerna för bakgrund, uppspelning och inläsning:

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

**CSS-egenskaper för spåret**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på motsvarande spår. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Färgen på motsvarande spår. </p> </td> 
  </tr> 
 </tbody> 
</table>

Följande CSS-klassväljare styr ratten:

```
.s7videoviewer .s7videoscrubber .s7knob
```

**CSS-egenskaper för ratten**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> övre </span> </p> </td> 
   <td colname="col2"> <p>Lodrät rattförskjutning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på ratten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjd på ratten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Knacka teckningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Följande CSS-klassväljare styr den tid som spelas upp:

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**CSS-egenskaper för bubblan för uppspelning**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Den teckensnittsfamilj som ska användas för visningstexten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> Den teckensnittsstorlek som ska användas för visningstexten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p> Teckenfärgen som ska användas för visningstexten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på bubbelområde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Bubbelområdets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Utfyllnad för bubbelområde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Bubbelteckningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> textjustering </span> </p> </td> 
   <td colname="col2"> <p>Textens justering mot bubbelområdet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Verktygstipset för videospolning kan lokaliseras. Mer information finns i [Lokalisering av användargränssnittselement](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

**Exempel** - Om du vill ställa in ett videovisningsprogram med en videonavigeringsruta med anpassade spårfärger. Rutningen måste vara tio pixlar hög och placerad tio pixlar och 35 pixlar från kontrollfältets övre och vänstra kant.

```
.s7videoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7videoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7videoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7videoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

När videofiltrering är aktiverat med parametern `navigation` visas kapitelplatser som markörer ovanpå videonavigeringsspåret.

Videokapitelmarkören styrs av följande CSS-klassväljare:

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

**CSS-egenskaper för videokapitelmarkören**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på videokapitelmarkör. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjd på videokapitelmarkör. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Grafik för videokapitelmarkörer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder både attributväljaren `state`, som du kan använda för att använda olika skal för olika knapplägen. I synnerhet motsvarar `selected='default'` standardläget för videokapitelmarkör och `selected='over'` används när videokapitelmarkören aktiveras av en muspekare eller en pekgest.

**Exempel** - Om du vill ställa in en videokapitelmarkör som är 5 x 8 pixlar och använder olika teckningar för läget&quot;default&quot; och&quot;over&quot;.

```
.s7videoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

Videokassubben placeras ovanpå videokapitelmarkören och visar titeln, starttiden och beskrivningen för ett visst kapitel. Det går att styra maximal bubbelbredd och lodrät förskjutning i förhållande till videonavigeringsspåret. Resten beräknas automatiskt av komponenten.

Videokassubblan styrs av följande CSS-klassväljare:

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**CSS-egenskaper för videokapitelbubblan**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p>Högsta bredd för videokapitelbubblan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p>Lodrät förskjutning från videonavigeringsspåret. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exempel** - Om du vill ställa in en videokapitelbubbla som är 235 pixlar bred och har åtta pixlar uppåt från videonavigeringsspårets underkant.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

Videokassubben består av ett valfritt sidhuvud och -innehåll. Rubriken har den valfria kapitelstarttiden och kapiteltiteln.

Rubriken styrs av följande CSS-klassväljare:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**CSS-egenskaper för videokapitelbubblans sidhuvud**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjd på videokapitelbubbla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad för videokapitelsidhuvudstext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärg för videokapitelbubblans sidhuvud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Höjd på textraden i videokapitelbubblans sidhuvud. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exempel** - Om du vill ställa in ett videokapitelbubbelhuvud som är 22 pixlar högt, en radhöjd på 22 pixlar, en vågrät marginal på 12 pixlar och en grå bakgrund.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

Starttiden för videokapitlet styrs av följande CSS-klassväljare:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**CSS-egenskaper för videokapitlets starttid**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Textfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Teckenbredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsfamilj. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnadshöger </span> </p> </td> 
   <td colname="col2"> <p> Utfyllnad mellan starttid och kapitelrubrik. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exempel** - Om du vill ange kapitelstarttid med det grå teckensnittet 10 pixlar Verdana och har utfyllnaden 10 pixlar till höger.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

Videoklippets titel styrs av följande CSS-klassväljare:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**CSS-egenskaper för videokapitelrubriken**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Textfärg för videokapitelrubrik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsbredd för videokapitelrubrik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsstorlek för videokapitelrubrik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsfamilj för videokapitelrubriker. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exempel** - Om du vill ställa in en videokapitelrubrik som använder ett vitt, fetstilt teckensnitt med tio pixlar Verdana.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

Beskrivningen av videokapitlet styrs av följande CSS-klassväljare:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
```

**CSS-egenskaper i videokapitelbeskrivningen**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Textfärg för videokapitelbeskrivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärg i videokapitelbeskrivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsbredd för videokapitelbeskrivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsstorlek för beskrivning av videokapitel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsfamilj för videokapitelbeskrivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Radhöjd för videokapitelbeskrivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utfyllnad </span> </p> </td> 
   <td colname="col2"> <p>Inre utfyllnad för videokapitelbeskrivning. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exempel** - Om du vill ställa in kapitelbeskrivning för video med ett mörkgrått, 11 pixlar Verdana-teckensnitt med ljusgrå bakgrund. Slutligen används fem pixlars radhöjd, 12 pixlars vågrät utfyllnad, 12 pixlars övre utfyllnad och 9 pixlars nedre utfyllnad.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

Kassaanslutningen längst ned i kapitelbubblan styrs av följande CSS-klassväljare:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**CSS-egenskaper för Edge Connector**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>Konnektionens färg. </p> <p>Definieras som <span class="codeph"> &lt;color&gt; transparent </span> så att endast den översta kantsfärgen definieras och de återstående kantlinjerna förblir genomskinliga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> Bredd på kantkoppling. </p> <p>Definieras som <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> så att samma bredd bara definieras för den övre och vågräta kantlinjen och den nedre kantlinjebredden är <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p> Definierar endast en negativ nedre marginal. Den ska ha samma värde som <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exempel** - Så här ställer du in en grå, sex pixlars kilkopplingskontakt:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
