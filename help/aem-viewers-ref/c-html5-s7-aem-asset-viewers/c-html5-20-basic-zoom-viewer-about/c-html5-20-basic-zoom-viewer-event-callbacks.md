---
title: Händelseåteranrop
description: Händelseåteranrop
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 14b317ab-82fb-4f55-babe-72c24e6afc2c
source-git-commit: d5f1f05c36c1cb8a57b5a4bb8a9d066c20e32e75
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Händelseåteranrop{#event-callbacks}

Visningsprogrammet har stöd för JavaScript-händelseåteranrop som webbsidan använder för att spåra visningsprogrammets initieringsprocess eller körningsbeteende.

Återanropshanterare tilldelas genom att händelsenamn och motsvarande hanterarfunktioner skickas med `handlers` egenskap till `config` JSON-objekt i visningsprogrammets konstruktor. Du kan också använda `setHandlers()` API-metod.

Visningsprogramhändelser som stöds är bland annat följande:

* `initComplete` - aktiveras när visningsprograminitieringen är klar och alla interna komponenter skapas, så att det går att använda `getComponent()` API. Callback-hanteraren tar inga argument.

* `trackEvent` - utlöses varje gång en händelse inträffar i visningsprogrammet som kan hanteras av ett händelsespårningssystem, t.ex. Adobe Analytics. Callback-hanteraren har följande argument:

   * `objID {String}` används inte för närvarande.
   * `compClass {String}` används inte för närvarande.
   * `instName {String}` ett instansnamn för SDK-komponenten för visningsprogrammet som utlöste händelsen.
   * `timeStamp {Number}` händelsetidsstämpel.
   * `eventInfo {String}` händelsenyttolast.

Se även [BasicZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-basiczoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) och [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-b748b29eaafa463a9d1723cb7b86f0d9).
