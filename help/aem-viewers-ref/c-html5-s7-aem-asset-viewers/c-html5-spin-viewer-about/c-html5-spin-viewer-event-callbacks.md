---
title: Händelseåteranrop
description: Händelseåteranrop
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 26f1dd99-fee9-4a71-9ec1-cfd1e29cb886
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '147'
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

Se även [SpinViewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195) och [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef).
