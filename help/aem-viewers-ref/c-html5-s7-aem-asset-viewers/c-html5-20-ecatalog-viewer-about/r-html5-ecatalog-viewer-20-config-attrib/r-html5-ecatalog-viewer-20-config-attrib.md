---
title: Kommandoreferens - Konfigurationsattribut
description: Konfigurationsattributdokumentation för eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för eCatalog Viewer.

Alla konfigurationskommandon kan anges i URL:en eller med API-metoderna `setParam()`, `setParams()` eller båda. Du kan också ange alla konfigurationsattribut som anges i konfigurationsposten på serversidan.

För vissa konfigurationskommandon kan du prefix till dem med klassnamnet eller instansnamnet för motsvarande Viewer SDK-komponent. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till API-metoden `setContainerId()`. Dokumentationen innehåller ett valfritt prefix för sådana kommandon. Kommandot `zoomstep` beskrivs till exempel så här:

`[PageView.|<containerId>_pageView].zoomstep`

Det innebär att du kan använda kommandot som

* `zoomstep` (kort syntax)
* `PageView.zoomstep` (kvalificerad med komponentklassnamn)
* `cont_pageView.zoomstep` (kvalificerad med komponent-ID, förutsatt att `cont` är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
