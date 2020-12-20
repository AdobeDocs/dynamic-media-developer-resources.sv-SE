---
description: JavaScript API-referens för Video Viewer
seo-description: JavaScript API-referens för Video Viewer
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: 083e4267-e296-454a-93a1-f0abf24cee94
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# getComponent{#getcomponent}

JavaScript API-referens för Video Viewer

`getComponent(componentId)`

Returnerar en referens till SDK-komponenten för visningsprogrammet som används av visningsprogrammet. Webbsidan kan använda den här metoden för att utöka eller anpassa beteendet för visningsprogrammet som inte är installerat. Anropa den här metoden först efter att återanropet för visningsprogrammet `initComplete` har körts, annars kanske komponenten inte har skapats ännu av visningsprogramlogiken.

## Parametrar {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`componentID`*`  -  `{String}` ett ID för SDK-komponenten för visningsprogrammet som används av visningsprogrammet. Detta visningsprogram stöder följande komponent-ID:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Komponent-ID </p> </th> 
   <th colname="col2" class="entry"> <p>Namn på SDK-komponentklass för visningsprogram </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färgrutor  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> setIndicator  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.SetIndicator  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomInButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomOutButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

När du arbetar med SDK-API:er är det viktigt att du använder rätt fullständigt kvalificerat SDK-namnutrymme enligt beskrivningen i [SDK-namnutrymme för visningsprogram](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-namespace.md#concept-53e47e46d7954e2b9681d13d716fd1ca).

Mer information om en viss komponent finns i dokumentationen till SDK API:t för visningsprogrammet.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` en referens till SDK-komponenten för visningsprogrammet. Metoden returnerar `null` om `componentId` inte är en visningsprogramkomponent som stöds eller om komponenten ännu inte har skapats av visningsprogramlogiken.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```

