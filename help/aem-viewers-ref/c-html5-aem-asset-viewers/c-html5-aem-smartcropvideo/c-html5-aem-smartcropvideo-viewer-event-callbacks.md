---
title: Händelseåteranrop
description: Händelseåteranrop
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 21962c01-f224-408d-8072-1c7f5d78ac4b
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '150'
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
   * `eventInfo {String}` händelsenyttolast.

Se även [SmartCropVideoViewer]
(/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md) och [setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md).
