---
description: Konfigurationsattributdokumentation för visningsprogrammet
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Flyout
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '152'
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
