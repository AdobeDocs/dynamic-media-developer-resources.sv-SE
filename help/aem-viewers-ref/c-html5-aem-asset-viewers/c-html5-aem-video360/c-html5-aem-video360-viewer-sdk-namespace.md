---
title: Namnutrymme för visningsprogramsDK
description: Namnutrymme för visningsprogramsDK
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 3360a3bd-8a4a-4bf9-98bf-ada7c35c58f4
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Namnutrymme för visningsprogramsDK{#viewer-sdk-namespace}

Visningsprogrammet är byggt av många SDK-komponenter för visningsprogrammet. Normalt behöver webbsidan inte interagera direkt med SDK-komponenternas API. alla vanliga behov behandlas i visningsprogrammets API.

Vissa avancerade användningsfall kräver dock att webbsidan refererar till en intern SDK-komponent som använder visningsprogrammets API `getComponent()` och sedan använder alla flexibiliteten i SDK:ernas API:er.

Namnutrymmet som används för att läsa in och initiera SDK-komponenter av visningsprogrammet beror på i vilken miljö visningsprogrammet körs. Om visningsprogrammet körs i Adobe Experience Manager läser visningsprogrammet in SDK-komponenter i namnutrymmet `s7viewers.s7sdk`. På samma sätt läser visningsprogrammet från Dynamic Media Classic in SDK:n i `s7classic.s7sdk`.

I båda fallen har det namnutrymme som används av SDK i visningsprogrammet antingen `s7viewers` eller `s7classic` som prefix. Den skiljer sig dessutom från det vanliga namnutrymmet `s7sdk` som används i SDK-användarhandboken eller SDK API-dokumentationen.

Därför är det viktigt att använda ett fullständigt kvalificerat SDK-namnutrymme när du skriver anpassad programkod som kommunicerar med interna visningsprogramkomponenter.

Om du till exempel tänker lyssna på händelsen `StatusEvent.NOTF_VIEW_READY` och visningsprogrammet hanteras från Experience Manager är den fullständigt kvalificerade händelsetypen `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` och händelseavlyssnarkoden ser ut ungefär så här:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
