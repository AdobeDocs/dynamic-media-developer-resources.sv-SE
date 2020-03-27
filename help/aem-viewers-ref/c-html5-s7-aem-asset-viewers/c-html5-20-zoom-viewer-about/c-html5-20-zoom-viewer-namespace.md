---
description: 'null'
seo-description: 'null'
seo-title: Namnutrymme för visningsprogramsDK
solution: Experience Manager
title: Namnutrymme för visningsprogramsDK
topic: Dynamic media
uuid: 29987da2-4535-47f3-a5ae-912c7cd10c86
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Namnutrymme för visningsprogramsDK{#viewer-sdk-namespace}

Visningsprogrammet är byggt av många SDK-komponenter för visningsprogrammet. I de flesta fall behöver webbsidan inte interagera direkt med SDK-komponenternas API. alla vanliga behov behandlas i visningsprogrammets API.

Vissa avancerade användningsfall kräver dock att webbsidan hämtar en referens till en intern SDK-komponent med `getComponent()` visningsprogrammets API och sedan använder alla de flexibla API:erna för SDK.

Namnutrymmet som används för att läsa in och initiera SDK-komponenter av visningsprogrammet beror på i vilken miljö visningsprogrammet körs. Om visningsprogrammet körs i AEM (Adobe Experience Manager) läser visningsprogrammet in SDK-komponenter i `s7viewers.s7sdk` namnutrymmet. På samma sätt läser visningsprogrammet från Scene7 Publishing System in SDK i `s7classic.s7sdk`.

I båda fallen har det namnutrymme som används av SDK:n i visningsprogrammet antingen `s7viewers` eller `s7classic` som prefix. Den skiljer sig dessutom från det vanliga `s7sdk` namnutrymmet som används i SDK-användarhandboken eller SDK API-dokumentationen. Därför är det viktigt att använda ett fullständigt kvalificerat SDK-namnutrymme när du skriver anpassad programkod som kommunicerar med interna visningsprogramkomponenter.

Om du till exempel tänker lyssna på `StatusEvent.NOTF_VIEW_READY` händelsen och visningsprogrammet hanteras från AEM, är den fullständigt kvalificerade händelsetypen `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`och händelseavlyssnarkoden ser ut ungefär så här:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Scene7 Publishing System will look like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

