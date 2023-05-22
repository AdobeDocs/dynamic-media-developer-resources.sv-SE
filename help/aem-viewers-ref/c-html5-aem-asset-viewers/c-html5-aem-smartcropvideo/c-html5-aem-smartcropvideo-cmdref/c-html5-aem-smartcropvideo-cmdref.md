---
title: Kommandoreferens - Konfigurationsattribut
description: Konfigurationsattributdokumentation för visningsprogrammet för Smart Crop Video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
mini-toc-levels: 3
exl-id: 698c03b1-bec0-44bf-9c79-c66e0192344a
source-git-commit: eaf59166fcc1ff8ec5a2e846ef0eb180c8cbdd5a
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för visningsprogrammet för Smart Crop Video.

Du kan ange valfritt konfigurationskommando i URL:en. Du kan också använda API-metoderna `setParam()`, eller `setParams()`eller båda för att ange ett konfigurationskommando. Du kan också ange valfritt config-attribut i konfigurationsposten på serversidan.

Du kan prefix för vissa konfigurationskommandon med klassnamnet eller instansnamnet för motsvarande Viewer SDK-komponent. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till `setContainerId()` API-metod. Dokumentationen innehåller valfria prefix för sådana kommandon. Till exempel: `playback` dokumenteras enligt följande:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Det innebär att det här kommandot används på följande sätt:

* `playback` (kort syntax)
* `SmartCropVideoPlayer.playback` (kvalificerad med komponentklassnamn)
* `cont_videoPlayer.playback` (kvalificerad med komponent-ID, förutsatt att `cont` är behållarelementets ID)

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Se [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
