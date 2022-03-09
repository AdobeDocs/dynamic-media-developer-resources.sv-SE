---
description: Namnutrymme för visningsprogramsDK
solution: Experience Manager
title: Namnutrymme för visningsprogramsDK
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Namnutrymme för visningsprogramsDK{#viewer-sdk-namespace}

Visningsprogrammet är byggt av många SDK-komponenter för visningsprogrammet. I de flesta fall behöver webbsidan inte interagera direkt med SDK-komponenternas API. alla vanliga behov behandlas i visningsprogrammets API.

Vissa avancerade användningsfall kräver dock att webbsidan hämtar en referens till en intern SDK-komponent med `getComponent()` API för visningsprogrammet och använd sedan SDK:ernas egna API:er på ett flexibelt sätt.

Namnutrymmet som används för att läsa in och initiera SDK-komponenter av visningsprogrammet beror på i vilken miljö visningsprogrammet körs. Om visningsprogrammet körs i AEM (Adobe Experience Manager) läser visningsprogrammet in SDK-komponenter i `s7viewers.s7sdk` namnutrymme. Och läsaren från Dynamic Media Classic läser in SDK:n i `s7classic.s7sdk`.

I båda fallen har namnutrymmet som används av SDK:n i visningsprogrammet antingen `s7viewers` eller `s7classic` som prefix. Och det skiljer sig från det vanliga `s7sdk` det namnutrymme som används i SDK-användarhandboken eller SDK API-dokumentationen.

Därför är det viktigt att använda ett fullständigt kvalificerat SDK-namnutrymme när du skriver anpassad programkod som kommunicerar med interna visningsprogramkomponenter.

Om du till exempel tänker lyssna på `StatusEvent.NOTF_VIEW_READY` -händelsen och visningsprogrammet hanteras från Dynamic Media Classic. Den fullständiga händelsetypen är `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`och händelseavlyssnarkoden ser ut ungefär så här:

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
