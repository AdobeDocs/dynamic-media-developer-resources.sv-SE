---
description: Konfigurationsattributdokumentation för Video Viewer.
seo-description: Konfigurationsattributdokumentation för Video Viewer.
seo-title: Kommandoreferens - Konfigurationsattribut
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
topic: Dynamic media
uuid: 837cf230-f7dd-4010-a299-c3267d11e200
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för Video Viewer.

Du kan ange valfritt konfigurationskommando i URL:en. Du kan också använda API-metoderna `setParam()`, `setParams()` eller båda för att ange ett konfigurationskommando. Du kan också ange valfritt config-attribut i konfigurationsposten på serversidan.

Du kan prefix för vissa konfigurationskommandon med klassnamnet eller instansnamnet för motsvarande Viewer SDK-komponent. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till API-metoden `setContainerId()`. Dokumentationen innehåller valfria prefix för sådana kommandon. `playback` dokumenteras till exempel enligt följande:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

vilket innebär att det här kommandot används på följande sätt:

* `playback` (kort syntax)
* `VideoPlayer.playback` (kvalificerad med komponentklassnamn)
* `cont_videoPlayer.playback` (kvalificerad med komponent-ID, förutsatt att det  `cont` är behållarelementets ID)

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Se [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
