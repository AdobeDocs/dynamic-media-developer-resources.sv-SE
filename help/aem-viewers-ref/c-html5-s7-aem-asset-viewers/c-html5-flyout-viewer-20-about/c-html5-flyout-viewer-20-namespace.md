---
title: Namnutrymme för visningsprogramsDK
description: Namnutrymme för visningsprogramsDK
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 06a7110a-3a6f-42f9-b729-e8f96762c64e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Namnutrymme för visningsprogramsDK{#viewer-sdk-namespace}

Visningsprogrammet är byggt av många SDK-komponenter för visningsprogrammet. Vanligtvis behöver webbsidan inte interagera direkt med SDK-komponenternas API. Alla vanliga behov behandlas i själva visningsprogrammets API.

Vissa avancerade användningsfall kräver dock att webbsidan refererar till en intern SDK-komponent som använder `getComponent()`-visningsprogrammets API och sedan använder all flexibilitet som finns i SDK:s API:er.

Namnutrymmet som används för att läsa in och initiera SDK-komponenter av visningsprogrammet beror på i vilken miljö visningsprogrammet körs. Om visningsprogrammet körs i Adobe Experience Manager läser visningsprogrammet in SDK-komponenter i namnområdet `s7viewers.s7sdk`. På samma sätt läser visningsprogrammet från Dynamic Media Classic in SDK:n i `s7classic.s7sdk`.

I båda fallen har det namnutrymme som används av SDK i visningsprogrammet antingen `s7viewers` eller `s7classic` som prefix. Den skiljer sig dessutom från det vanliga namnutrymmet `s7sdk` som används i SDK-användarhandboken eller SDK API-dokumentationen. Därför är det viktigt att använda ett fullständigt kvalificerat SDK-namnutrymme när du skriver anpassad programkod som kommunicerar med interna visningsprogramkomponenter.

Om du till exempel tänker lyssna på händelsen `StatusEvent.NOTF_VIEW_READY` och visningsprogrammet hanteras från Experience Manager är den fullständigt kvalificerade händelsetypen `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` och händelseavlyssnarkoden ser ut ungefär så här:

```html {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic looks like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
