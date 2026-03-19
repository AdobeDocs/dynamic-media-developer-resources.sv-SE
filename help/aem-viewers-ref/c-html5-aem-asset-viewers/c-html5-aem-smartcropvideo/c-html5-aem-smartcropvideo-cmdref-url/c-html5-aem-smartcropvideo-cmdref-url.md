---
title: Kommandoreferens - URL
description: Kommandoreferensdokumentation för visningsprogrammet för smart beskärning.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: d0797c10-2379-45f7-9e8d-a5eb56638db8
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Kommandoreferens - URL{#command-reference-url}

Kommandoreferensdokumentation för visningsprogrammet för smart beskärning.

Du kan ange valfritt konfigurationskommando i URL:en. Du kan också använda API-metoderna `setParam()`, `setParams()` eller båda för att ange ett konfigurationskommando. Du kan också ange valfritt config-attribut i konfigurationsposten på serversidan.

Du kan prefix för vissa konfigurationskommandon med klassnamnet eller instansnamnet för motsvarande Viewer SDK-komponent. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till API-metoden `setContainerId()`. Dokumentationen innehåller valfria prefix för sådana kommandon. `playback` dokumenteras till exempel enligt följande:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Det innebär att det här kommandot används på följande sätt:

* `playback` (kort syntax)
* `SmartCropVideoPlayer.playback` (kvalificerad med komponentklassnamn)
* `cont_smartCropVideoPlayer.playback` (kvalificerad med komponent-ID, förutsatt att `cont` är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Se även [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
