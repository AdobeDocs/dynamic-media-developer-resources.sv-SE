---
description: Kommandoreferensdokumentation för Interactive Video Viewer.
seo-description: Kommandoreferensdokumentation för Interactive Video Viewer.
seo-title: Kommandoreferens - URL
solution: Experience Manager
title: Kommandoreferens - URL
topic: Dynamic media
uuid: 4f9e4a79-6865-4e41-b30b-84ff2c6f6045
translation-type: tm+mt
source-git-commit: 3266e8682711dac379a09a0e992d33b8ffc7b5a4

---


# Kommandoreferens - URL{#command-reference-url}

Kommandoreferensdokumentation för Interactive Video Viewer.

Du kan ange valfritt konfigurationskommando i URL:en. Du kan också använda API-metoderna `setParam()`, `setParams()`eller båda, för att ange ett konfigurationskommando. Du kan också ange valfritt config-attribut i konfigurationsposten på serversidan.

Du kan prefix för vissa konfigurationskommandon med klassnamnet eller instansnamnet för motsvarande Viewer SDK-komponent. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till `setContainerId()` API-metoden. Dokumentationen innehåller valfria prefix för sådana kommandon. Följande `playback` dokumenteras:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

vilket innebär att det här kommandot används på följande sätt:

* `playback` (kort syntax)
* `VideoPlayer.playback` (kvalificerad med komponentklassnamn)
* `cont_videoPlayer.playback` (kvalificerad med komponent-ID, förutsatt att det `cont` är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Se även [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
