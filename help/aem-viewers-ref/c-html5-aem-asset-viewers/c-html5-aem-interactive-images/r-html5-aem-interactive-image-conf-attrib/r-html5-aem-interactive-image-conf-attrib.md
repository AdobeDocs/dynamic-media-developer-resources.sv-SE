---
title: Kommandoreferens - Konfigurationsattribut
description: Konfigurationsattributdokumentation för Interactive Image Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för Interactive Image Viewer.

Alla konfigurationskommandon kan anges i URL eller med `setParam()`, eller `setParams()`, eller båda, API-metoder. Alla config-attribut kan också anges i konfigurationsposten på serversidan.

Vissa konfigurationskommandon kan ha prefixet med klassnamnet eller instansnamnet för motsvarande SDK-komponent i visningsprogrammet. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till `setContainerId()` API-metod. Dokumentationen innehåller ett valfritt prefix för sådana kommandon. Till exempel: `zoomstep` kommandot dokumenteras enligt följande:

`[ZoomView.|<containerId>_zoomView].fmt`

Betyder att du kan använda det här kommandot som:

* `fmt` (kort syntax)
* `ZoomView.fmt` (kvalificerad med komponentklassnamn)
* `cont_zoomView.fmt` (kvalificerad med komponent-ID, antar `cont` är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
