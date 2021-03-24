---
description: JavaScript API-referens för Video360 Viewer.
solution: Experience Manager
title: Video360Viewer
feature: Dynamic Media Classic,visningsprogram,SDK/API,360 VR-video
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Video360Viewer{#video-viewer}

JavaScript API-referens för Video360 Viewer.

`Video360Viewer([config])`

Konstruktorn skapar en ny HTML5 Video360-visningsprograminstans.

## Parametrar {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object}  </span> valfritt JSON-konfigurationsobjekt, tillåter alla visningsprograminställningar att skicka till konstruktorn för att undvika anrop av enskilda set-metoder. Innehåller följande egenskaper: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID för DOM-behållaren (vanligtvis en  <span class="codeph"> DIV  </span>) som visningsprogrammet infogas i. När den här metoden anropas är det inte nödvändigt att skapa behållarelementet. Behållaren måste dock finnas när <span class="codeph"> init() </span> körs. </p> <p>Obligatoriskt. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params  </span> -  <span class="codeph"> {Object}  </span> JSON-objekt med visarkonfigurationsparametrar där egenskapsnamnet antingen är visningsprogramsspecifikt konfigurationsalternativ eller SDK-modifierare, och värdet för den egenskapen är ett motsvarande inställningsvärde. </p> <p>Obligatoriskt. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> hanterare  </span> -  <span class="codeph"> {Object}  </span> JSON-objekt med återkopplingar för visningsprogramhändelser, där egenskapsnamnet är namnet på den visningsprogramhändelse som stöds och egenskapsvärdet är en JavaScript-funktionsreferens till lämpligt återanrop. </p> <p>Valfritt. </p> <p>Mer information om visningsprogramhändelser finns i <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Händelseåteranrop </a>. </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedTexts  </span> -  <span class="codeph"> {Object}  </span> JSON-objekt med lokaliseringsdata. Valfritt. </p> <p>Mer information finns i <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Lokalisering av användargränssnittselement </a>. </p> <p>Se även <i>Användarhandboken för visningsprogrammet SDK</i> och exemplet för mer information om objektets innehåll. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```

