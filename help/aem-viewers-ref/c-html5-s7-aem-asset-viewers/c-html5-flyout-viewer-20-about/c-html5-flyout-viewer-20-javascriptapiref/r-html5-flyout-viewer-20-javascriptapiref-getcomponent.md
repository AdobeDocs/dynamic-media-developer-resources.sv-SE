---
description: JavaScript API-referens för visningsprogrammet
solution: Experience Manager
title: getComponent
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# getComponent{#getcomponent}

JavaScript API-referens för visningsprogrammet

`getComponent(componentId)`

Returnerar en referens till SDK-komponenten för visningsprogrammet som används av visningsprogrammet. Webbsidan kan använda den här metoden för att utöka eller anpassa beteendet för visningsprogrammet som inte är installerat. Anropa den här metoden först efter att återanropet för visningsprogrammet `initComplete` har körts. Annars kanske komponenten inte har skapats ännu av visningsprogramlogiken.

## Parametrar {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*`  -  `{String}` ett ID för SDK-komponenten för visningsprogrammet som används av visningsprogrammet. Detta visningsprogram stöder följande komponent-ID:

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
   <td colname="col1"> <p> <span class="codeph"> utfällbar  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.FlyoutZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färgrutor  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

När du arbetar med SDK API:er är det viktigt att du använder ett korrekt, fullständigt kvalificerat SDK-namnutrymme enligt beskrivningen i [Viewer SDK](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-namespace.md#concept-453501a601634dd1bca7b96878c22605).

Mer information om en viss komponent finns i dokumentationen för SDK-API:t för visningsprogrammet.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` en referens till SDK-komponenten för visningsprogrammet. Metoden returnerar `null` om `componentId` inte är en visningsprogramkomponent som stöds eller om komponenten ännu inte har skapats av visningsprogramlogiken.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyoutZoomView = <instance>.getComponent("flyout"); 
} 
})
```

