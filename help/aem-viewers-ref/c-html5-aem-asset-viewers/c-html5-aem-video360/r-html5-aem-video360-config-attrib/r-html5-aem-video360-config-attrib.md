---
title: Kommandoreferens - Konfigurationsattribut
description: Konfigurationsattributdokumentation för Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för Video360 Viewer.

Alla konfigurationskommandon kan anges i URL eller med `setParam()`, eller `setParams()`, eller båda, API-metoder. Alla konfigurationsattribut kan också anges i konfigurationsposten på serversidan.

Vissa konfigurationskommandon kan ha prefixet med klassnamnet eller instansnamnet för motsvarande SDK-komponent i visningsprogrammet. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till `setContainerId()` API-metod. Dokumentationen innehåller ett valfritt prefix för sådana kommandon. Till exempel: `playback` kommandot dokumenteras enligt följande:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

Det betyder att du kan använda det här kommandot i följande:

* `playback` (kort syntax)
* `VideoPlayer.playback` (kvalificerad med komponentklassnamn)
* `cont_videoPlayer.playback` (kvalificerad med komponent-ID, antar `cont` är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
