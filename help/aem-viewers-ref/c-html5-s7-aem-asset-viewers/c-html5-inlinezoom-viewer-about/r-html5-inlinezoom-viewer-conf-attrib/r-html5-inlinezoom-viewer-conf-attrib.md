---
description: Konfigurationsattributdokumentation för visningsprogrammet
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Textbunden zoom
role: Developer,User
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '150'
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
