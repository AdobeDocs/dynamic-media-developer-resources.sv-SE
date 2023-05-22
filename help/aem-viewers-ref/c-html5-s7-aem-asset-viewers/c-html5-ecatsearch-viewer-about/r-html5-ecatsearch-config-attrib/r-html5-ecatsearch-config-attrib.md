---
description: Konfigurationsattributdokumentation för eCatalog Viewer.
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för eCatalog Viewer.

Alla konfigurationskommandon kan anges i URL eller med `setParam()`, eller `setParams()`, eller båda, API-metoder. Du kan också ange alla konfigurationsattribut som anges i konfigurationsposten på serversidan.

För vissa konfigurationskommandon kan du prefix till dem med klassnamnet eller instansnamnet för motsvarande Viewer SDK-komponent. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till `setContainerId()` API-metod. Dokumentationen innehåller valfria prefix för sådana kommandon. Till exempel: `zoomstep` kommandot dokumenteras enligt följande:

`[PageView.|<containerId>_pageView].zoomstep`

vilket betyder att du kan använda det här kommandot som:

* `zoomstep` (kort syntax)
* `PageView.zoomstep` (kvalificerad med komponentklassnamn)
* `cont_pageView.zoomstep` (kvalificerad med komponent-ID, antar `cont` är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
