---
description: Händelseåteranrop
solution: Experience Manager
title: Händelseåteranrop
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Zoom
role: Developer,User
exl-id: 68aa55da-5f6f-4c7d-8d3f-c25de9cc325c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# Händelseåteranrop{#event-callbacks}

Visningsprogrammet har stöd för JavaScript-händelseåteranrop som webbsidan använder för att spåra visningsprogrammets initieringsprocess eller körningsbeteende.

Återanropshanterare tilldelas genom att händelsenamn och motsvarande hanterarfunktioner med egenskapen `handlers` skickas till JSON-objektet `config` i visningsprogrammets konstruktor. Du kan också använda API-metoden `setHandlers()`.

Visningsprogramhändelser som stöds är bland annat följande:

* `initComplete` - utlöses när visningsprograminitieringen är klar och alla interna komponenter skapas, så att det går att använda  `getComponent()` API. Callback-hanteraren tar inga argument.

* `trackEvent` - utlöses varje gång en händelse inträffar i visningsprogrammet som kan hanteras av ett händelsespårningssystem, t.ex. Adobe Analytics. Callback-hanteraren har följande argument:

   * `objID {String}` används inte för närvarande.
   * `compClass {String}` används inte för närvarande.
   * `instName {String}` ett instansnamn för SDK-komponenten för visningsprogrammet som utlöste händelsen.
   * `timeStamp {Number}` händelsetidsstämpel.
   * `eventInfo {String}` händelsenyttolast.

Se även [ZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-zoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) och [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
