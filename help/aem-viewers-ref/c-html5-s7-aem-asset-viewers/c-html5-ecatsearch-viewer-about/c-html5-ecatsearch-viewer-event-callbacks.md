---
description: 'null'
seo-description: 'null'
seo-title: Händelseåteranrop
solution: Experience Manager
title: Händelseåteranrop
topic: Dynamic media
uuid: 0c4c4111-5ad7-458c-afa2-d551b5987322
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '149'
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

Se även [eCatalogViewer](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-javascriptapiref/r-html5-ecatsearch-javascriptapiref-ecatalogsearchviewer.md) och [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856).
