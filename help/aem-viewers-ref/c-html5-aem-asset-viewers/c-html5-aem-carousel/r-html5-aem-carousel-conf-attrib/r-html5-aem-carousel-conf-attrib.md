---
description: Konfigurationsattributdokumentation för Carousel Viewer.
seo-description: Konfigurationsattributdokumentation för Carousel Viewer.
seo-title: Kommandoreferens - Konfigurationsattribut
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
topic: Dynamic media
uuid: 036af728-ab00-4db3-98cf-d16f1bffa064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för Carousel Viewer.

Alla konfigurationskommandon kan anges i URL eller med `setParam()`, eller `setParams()`båda, API-metoder. Alla config-attribut kan också anges i konfigurationsposten på serversidan.

Vissa konfigurationskommandon kan ha prefixet med klassnamnet eller instansnamnet för motsvarande SDK-komponent i visningsprogrammet. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till `setContainerId()` API-metoden. Dokumentationen innehåller ett valfritt prefix för sådana kommandon. Kommandot beskrivs till exempel på följande sätt `zoomstep` :

`[ZoomView.|<containerId>_carouselView].fmt`

vilket betyder att du kan använda det här kommandot som:

* `fmt` (kort syntax)
* `CarouselView.fmt` (kvalificerad med komponentklassnamn)
* `cont_carouselView.fmt` (kvalificerad med komponent-ID, förutsatt `cont` att är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
