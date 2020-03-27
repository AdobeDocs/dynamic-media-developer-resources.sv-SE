---
description: JavaScript API-referens för Carousel Viewer.
seo-description: JavaScript API-referens för Carousel Viewer.
seo-title: getComponent**
solution: Experience Manager
title: getComponent**
topic: Dynamic media
uuid: b5449564-c01c-4bb3-b265-b8d70e5f1b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getComponent**{#getcomponent}

JavaScript API-referens för Carousel Viewer.

`getComponent(componentId)`

Returnerar en referens till SDK-komponenten för visningsprogrammet som används av visningsprogrammet. Webbsidan kan använda den här metoden för att utöka eller anpassa beteendet för visningsprogrammet som inte är installerat. Anropa den här metoden först efter att `initComplete` visningsprogrammets återanrop har körts, annars kanske komponenten inte har skapats ännu av visningsprogramlogiken.

## Parametrar {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`componentID`*` - `{String}` ett ID för SDK-komponenten för visningsprogrammet som används av visningsprogrammet. Detta visningsprogram stöder följande komponent-ID:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Komponent-ID </p> </th> 
   <th colname="col2" class="entry"> <p>Namn på SDK-komponentklass för visningsprogram </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> carouselView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.CarouselView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> controlBar </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> setIndicator </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.SetIndicator </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nextButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> prevButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

När du arbetar med SDK API:er är det viktigt att du använder rätt fullständigt kvalificerat SDK-namnutrymme enligt beskrivningen i [visningsprogrammets SDK-namnutrymme](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-namespace.md).

Mer information om en viss komponent finns i dokumentationen till SDK API:t för visningsprogrammet.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` en referens till SDK-komponenten för visningsprogrammet. Metoden returnerar `null` om `componentId` inte är en visningsprogramkomponent som stöds eller om komponenten ännu inte har skapats av visningsprogramlogiken.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
} 
})
```

