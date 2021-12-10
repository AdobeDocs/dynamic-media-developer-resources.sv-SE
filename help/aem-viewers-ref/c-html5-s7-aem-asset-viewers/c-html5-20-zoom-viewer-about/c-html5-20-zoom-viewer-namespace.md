---
title: Namnutrymme för visningsprogramsDK
description: Namnutrymme för visningsprogramsDK
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ad68dd09-d8df-4fc8-952a-ef82d9662de9
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Namnutrymme för visningsprogramsDK{#viewer-sdk-namespace}

Visningsprogrammet är byggt av många SDK-komponenter för visningsprogrammet. Normalt behöver webbsidan inte interagera direkt med SDK-komponenternas API. alla vanliga behov behandlas i visningsprogrammets API.

Vissa avancerade användningsfall kräver dock att webbsidan refererar till en intern SDK-komponent med `getComponent()` API för visningsprogrammet och använd sedan SDK:ernas egna API:er på ett flexibelt sätt.

Namnutrymmet som används för att läsa in och initiera SDK-komponenter av visningsprogrammet beror på i vilken miljö visningsprogrammet körs. Om visningsprogrammet körs i Adobe Experience Manager läser visningsprogrammet in SDK-komponenter i `s7viewers.s7sdk` namnutrymme. På samma sätt läser visningsprogrammet från Dynamic Media Classic in SDK i `s7classic.s7sdk`.

I båda fallen har namnutrymmet som används av SDK:n i visningsprogrammet antingen `s7viewers` eller `s7classic` som prefix. Och det skiljer sig från det vanliga `s7sdk` det namnutrymme som används i SDK-användarhandboken eller SDK API-dokumentationen. Därför är det viktigt att använda ett fullständigt kvalificerat SDK-namnutrymme när du skriver anpassad programkod som kommunicerar med interna visningsprogramkomponenter.

Om du till exempel tänker lyssna på `StatusEvent.NOTF_VIEW_READY` -händelsen och visningsprogrammet hanteras från Experience Manager, den fullständigt kvalificerade händelsetypen är `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`och händelseavlyssnarkoden ser ut ungefär så här:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic will look like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
