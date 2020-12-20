---
description: Konfigurationsattributdokumentation för eCatalog Viewer.
seo-description: Konfigurationsattributdokumentation för eCatalog Viewer.
seo-title: Kommandoreferens - Konfigurationsattribut
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
topic: Dynamic media
uuid: 823ad411-653a-44de-97de-147e3b27a917
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för eCatalog Viewer.

Alla konfigurationskommandon kan anges i URL:en eller med hjälp av API-metoderna `setParam()`, `setParams()` eller båda. Du kan också ange alla konfigurationsattribut som anges i konfigurationsposten på serversidan.

För vissa konfigurationskommandon kan du prefix till dem med klassnamnet eller instansnamnet för motsvarande Viewer SDK-komponent. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till API-metoden `setContainerId()`. Dokumentationen innehåller valfria prefix för sådana kommandon. Kommandot `zoomstep` beskrivs till exempel så här:

`[PageView.|<containerId>_pageView].zoomstep`

vilket betyder att du kan använda det här kommandot som:

* `zoomstep` (kort syntax)
* `PageView.zoomstep` (kvalificerad med komponentklassnamn)
* `cont_pageView.zoomstep` (kvalificerad med komponent-ID, förutsatt  `cont` att är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
