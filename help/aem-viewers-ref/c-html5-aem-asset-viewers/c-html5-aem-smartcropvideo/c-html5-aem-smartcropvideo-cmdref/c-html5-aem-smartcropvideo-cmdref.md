---
description: Konfigurationsattributdokumentation för visningsprogrammet för Smart Crop Video.
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 5992e5cd-7783-408e-a23f-fdcc3a3d6b69
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för visningsprogrammet för Smart Crop Video.

Du kan ange valfritt konfigurationskommando i URL:en. Du kan också använda API-metoderna `setParam()`, eller `setParams()`eller båda för att ange ett konfigurationskommando. Du kan också ange valfritt config-attribut i konfigurationsposten på serversidan.

Du kan prefix för vissa konfigurationskommandon med klassnamnet eller instansnamnet för motsvarande Viewer SDK-komponent. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till `setContainerId()` API-metod. Dokumentationen innehåller valfria prefix för sådana kommandon. Till exempel: `playback` dokumenteras enligt följande:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

vilket innebär att det här kommandot används på följande sätt:

* `playback` (kort syntax)
* `SmartCropVideoPlayer.playback` (kvalificerad med komponentklassnamn)
* `cont_videoPlayer.playback` (kvalificerad med komponent-ID, förutsatt att `cont` är behållarelementets ID)

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Se [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
