---
description: Namnutrymme för visningsprogramsDK
solution: Experience Manager
title: Namnutrymme för visningsprogramsDK
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---


# SDK-namnområde för visningsprogram{#viewer-sdk-namespace}

Visningsprogrammet är byggt av många SDK-komponenter för visningsprogrammet. I de flesta fall behöver webbsidan inte interagera direkt med SDK-komponenternas API. alla vanliga behov behandlas i visningsprogrammets API.

Vissa avancerade användningsfall kräver dock att webbsidan hämtar en referens till en intern SDK-komponent med hjälp av visningsprogrammets API `getComponent()` och sedan använder samma flexibilitet som programmeringsgränssnitten i SDK.

Namnutrymmet som används för att läsa in och initiera SDK-komponenter av visningsprogrammet beror på i vilken miljö visningsprogrammet körs. Om visningsprogrammet körs i AEM (Adobe Experience Manager) läser visningsprogrammet in SDK-komponenter i namnutrymmet `s7viewers.s7sdk`. Och visningsprogrammet som hanteras från Dynamic Media Classic läser in SDK:n till `s7classic.s7sdk`.

I båda fallen har det namnutrymme som används av SDK i visningsprogrammet antingen `s7viewers` eller `s7classic` som prefix. Den skiljer sig dessutom från det vanliga namnutrymmet `s7sdk` som används i SDK-användarhandboken eller SDK API-dokumentationen.

Därför är det viktigt att använda ett fullständigt kvalificerat SDK-namnutrymme när du skriver anpassad programkod som kommunicerar med interna visningsprogramkomponenter.

Om du till exempel tänker lyssna på händelsen `StatusEvent.NOTF_VIEW_READY` och visningsprogrammet hanteras från Dynamic Media Classic är den fullständigt kvalificerade händelsetypen `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY` och händelseavlyssnarkoden ser ut ungefär så här:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

