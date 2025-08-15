---
title: SDK-namnområde för visningsprogram
description: SDK-namnområde för visningsprogram
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 1712f08c-70e6-483e-a4e5-614448f35374
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# SDK-namnområde för visningsprogram{#viewer-sdk-namespace}

Visningsprogrammet består av många Viewer SDK-komponenter. Vanligtvis behöver webbsidan inte interagera direkt med API:t för SDK-komponenter. Alla vanliga behov behandlas i själva API:t för visningsprogrammet.

Vissa avancerade användningsfall kräver dock att webbsidan refererar till en intern SDK-komponent som använder `getComponent()`-visningsprogrammets API och sedan använder all flexibilitet i SDK egna API:er.

Det namnutrymme som används för att läsa in och initiera SDK-komponenter av visningsprogrammet beror på i vilken miljö visningsprogrammet körs. Om visningsprogrammet körs i Adobe Experience Manager läser visningsprogrammet in SDK-komponenter i namnområdet `s7viewers.s7sdk`. Visningsprogrammet från Dynamic Media Classic läser in SDK till `s7classic.s7sdk`.

I båda fallen har det namnutrymme som används av SDK i visningsprogrammet antingen `s7viewers` eller `s7classic` som prefix. Den skiljer sig dessutom från det vanliga namnutrymmet `s7sdk` som används i SDK användarhandbok eller i dokumentationen för SDK API.

Därför är det viktigt att du använder ett fullständigt kvalificerat SDK-namnutrymme när du skriver anpassad programkod som kommunicerar med interna visningsprogramkomponenter.

Om du till exempel tänker lyssna på händelsen `StatusEvent.NOTF_VIEW_READY` och visningsprogrammet hanteras från Experience Manager är den fullständigt kvalificerade händelsetypen `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` och händelseavlyssnarkoden ser ut ungefär så här:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
   carouselView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
