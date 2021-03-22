---
description: Konfigurationsattributdokumentation för visningsprogrammet
seo-description: Konfigurationsattributdokumentation för visningsprogrammet
seo-title: Kommandoreferens - Konfigurationsattribut
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
uuid: d7e89a24-a235-4f20-86d1-25aacd118880
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Flyout
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för visningsprogrammet

Du kan ange valfritt konfigurationskommando i URL:en. Eller så kan du använda `setParam()`, `setParams()` eller båda API-metoderna. Du kan också ange valfritt konfigurationsattribut i konfigurationsposten på serversidan.

Vissa konfigurationskommandon har prefixet med klassnamnet eller instansnamnet för motsvarande SDK-komponent i visningsprogrammet. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till API-metoden `setContainerId()`. Dokumentationen innehåller ett valfritt prefix för sådana kommandon. Kommandot `zoomfactor` beskrivs till exempel så här:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

Kommandot används enligt följande:

* `zoomfactor` (kort syntax)
* `FlyoutZoomView.zoomfactor` (kvalificerad med ett komponentklassnamn)
* `cont_flyout.zoomfactor` (kvalificerat med komponent-ID, förutsatt att det  `cont` är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
