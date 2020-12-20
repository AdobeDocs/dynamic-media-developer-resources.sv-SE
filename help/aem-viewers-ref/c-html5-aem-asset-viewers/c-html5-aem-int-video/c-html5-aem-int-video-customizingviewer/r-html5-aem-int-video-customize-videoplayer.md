---
description: Videospelaren är det rektangulära området där videoinnehållet visas i visningsprogrammet.
seo-description: Videospelaren är det rektangulära området där videoinnehållet visas i visningsprogrammet.
seo-title: Videospelare
solution: Experience Manager
title: Videospelare
topic: Dynamic media
uuid: ff0f78b1-ff88-47b8-a118-4e0b3e75f341
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---


# Videospelare{#video-player}

Videospelaren är det rektangulära området där videoinnehållet visas i visningsprogrammet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Om dimensionerna för videon som spelas upp inte matchar dimensionerna för videospelaren centreras videoinnehållet i videospelarens rektangulära visningsområde.

Följande CSS-klassväljare styr videospelarens utseende:

```
.s7interactivevideoviewer .s7videoplayer
```

**CSS-egenskaper för videospelaren**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Huvudvyns bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Du kan lokalisera felmeddelandet som visas om systemet inte kan spela upp videon.

Se [Lokalisering av element i användargränssnittet](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exempel - Om du vill ställa in ett videovisningsprogram med videospelarens storlek inställd på 512 x 288 pixlar.

```
.s7interactivevideoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

Undertexter placeras i en intern behållare inuti videospelaren. Placeringen av behållaren styrs av WebVTT-positioneringsoperatorer som stöds. Bildtexten finns inuti den behållaren och dess format styrs med följande CSS-klassväljare:

`.s7interactivevideoviewer .s7videoplayer .s7caption`

**CSS-egenskaper för undertextning**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Textbakgrund för dold text. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg  </span> </p> </td> 
   <td colname="col2"> <p>Stäng bildtextens färg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p> Teckensnittsbredd för dold bildtext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p> Teckensnittsstorlek för dold text. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Textningsteckensnitt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-5b82913ff3c44b7b8187969cb15e9560}

Så här ställer du in en textning som ska vara 14 pixlar, ljusgrå Arial, på en halvgenomskinlig svart bakgrund:

```
.s7interactivevideoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

Utseendet på buffringsanimeringen styrs med följande CSS-klassväljare:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon
```

**CSS-egenskaper för vänteikonen**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Animeringsikonens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> Höjd på animeringsikonen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-vänster  </span> </p> </td> 
   <td colname="col2"> <p> Animeringsikonens vänstermarginal, normalt minus halva ikonens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-top  </span> </p> </td> 
   <td colname="col2"> <p> Animeringsikonens övre marginal, normalt minus halva ikonens höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Knacka teckningar. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in en buffringsanimering som 101 pixlar bred och 29 pixlar hög:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

