---
title: Händelseåteranrop
description: Händelseåteranrop
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Händelseåteranrop{#event-callbacks}

Visningsprogrammet har stöd för JavaScript händelsereferenser som används på webbsidan för att spåra visningsprogrammets initieringsprocess eller körningsbeteende.

Återanropshanterare tilldelas genom att händelsenamn och motsvarande hanterarfunktioner skickas med egenskapen `handlers` till JSON-objektet `config` i visningsprogrammets konstruktor. Du kan också använda API-metoden `setHandlers()`.

Visningsprogramhändelser som stöds är bland annat följande:

* `initComplete` - utlöses när visningsprogrammets initiering är klar och alla interna komponenter skapas, så att det går att använda `getComponent()` API. Callback-hanteraren tar inga argument.
* `trackEvent` - utlöses varje gång en händelse inträffar i visningsprogrammet som kan hanteras av ett händelsespårningssystem, till exempel Adobe Analytics. Callback-hanteraren har följande argument:

   * `objID {String}` används inte just nu.
   * `compClass {String}` används inte just nu.
   * `instName {String}` ett instansnamn för SDK-komponenten för visningsprogrammet som utlöste händelsen.
   * `timeStamp {Number}`-händelsens tidsstämpel.
   * `eventInfo {String}` händelsenyttolast.

* `quickViewActivate` - utlöses när en användare klickar på eller trycker på en interaktiv färgruta i den interaktiva färgrutekomponenten eller i skärmen &quot;call to action&quot; som visas i slutet av videouppspelningen. Callback-hanteraren tar det enda argumentet som är ett JSON-objekt med följande fält:

   * `sku` `String` SKU-värde som är associerat med den interaktiva färgrutan.
   * `<additionalVariable>` { `String`} noll eller fler ytterligare variabler som är associerade med den interaktiva färgrutan.

Se även [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) och [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
