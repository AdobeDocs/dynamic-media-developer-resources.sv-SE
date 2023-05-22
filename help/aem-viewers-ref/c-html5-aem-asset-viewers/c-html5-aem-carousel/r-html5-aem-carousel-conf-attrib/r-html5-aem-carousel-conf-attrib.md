---
title: Kommandoreferens - Konfigurationsattribut
description: Konfigurationsattributdokumentation för Carousel Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 71c2c973-d711-4d37-b778-381a7ec71527
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för Carousel Viewer.

Alla konfigurationskommandon kan anges i URL eller med `setParam()`, eller `setParams()`, eller båda, API-metoder. Alla config-attribut kan också anges i konfigurationsposten på serversidan.

Vissa konfigurationskommandon kan ha prefixet med klassnamnet eller instansnamnet för motsvarande SDK-komponent i visningsprogrammet. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till `setContainerId()` API-metod. Dokumentationen innehåller ett valfritt prefix för sådana kommandon. Till exempel: `zoomstep` kommandot dokumenteras enligt följande:

`[ZoomView.|<containerId>_carouselView].fmt`

I så fall kan du använda det här kommandot:

* `fmt` (kort syntax)
* `CarouselView.fmt` (kvalificerad med komponentklassnamn)
* `cont_carouselView.fmt` (kvalificerad med komponent-ID, antar `cont` är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
