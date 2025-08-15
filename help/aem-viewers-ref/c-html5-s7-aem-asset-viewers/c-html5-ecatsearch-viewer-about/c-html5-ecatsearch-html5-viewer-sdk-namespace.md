---
description: SDK-namnområde för visningsprogram
solution: Experience Manager
title: SDK-namnområde för visningsprogram
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# SDK-namnområde för visningsprogram{#viewer-sdk-namespace}

Visningsprogrammet består av många Viewer SDK-komponenter. I de flesta fall behöver webbsidan inte interagera direkt med API:t för SDK-komponenter. Alla vanliga behov behandlas i själva API:t för visningsprogrammet.

För vissa avancerade användningsfall krävs dock att webbsidan hämtar en referens till en intern SDK-komponent med `getComponent()`-visningsprogrammets API och sedan använder alla de flexibla API:erna för SDK.

Det namnutrymme som används för att läsa in och initiera SDK-komponenter av visningsprogrammet beror på i vilken miljö visningsprogrammet körs. Om visningsprogrammet körs i AEM (Adobe Experience Manager) läser visningsprogrammet in SDK-komponenter i namnområdet `s7viewers.s7sdk`. Visningsprogrammet från Dynamic Media Classic läser in SDK till `s7classic.s7sdk`.

I båda fallen har det namnutrymme som används av SDK i visningsprogrammet antingen `s7viewers` eller `s7classic` som prefix. Den skiljer sig dessutom från det vanliga namnutrymmet `s7sdk` som används i SDK användarhandbok eller i dokumentationen för SDK API.

Därför är det viktigt att du använder ett fullständigt kvalificerat SDK-namnutrymme när du skriver anpassad programkod som kommunicerar med interna visningsprogramkomponenter.

Om du till exempel tänker lyssna på händelsen `StatusEvent.NOTF_VIEW_READY` och visningsprogrammet hanteras från Dynamic Media Classic är den fullständigt kvalificerade händelsetypen `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY` och händelseavlyssnarkoden ser ut ungefär så här:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
