---
description: Kommandoreferensdokumentation för visningsprogrammet för smart beskärning.
solution: Experience Manager
title: Kommandoreferens - URL
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 1ed78e0d-9b93-4c66-b558-fac15c51e944
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Kommandoreferens - URL{#command-reference-url}

Kommandoreferensdokumentation för visningsprogrammet för smart beskärning.

Du kan ange valfritt konfigurationskommando i URL:en. Du kan också använda API-metoderna `setParam()`, eller `setParams()`eller båda för att ange ett konfigurationskommando. Du kan också ange valfritt config-attribut i konfigurationsposten på serversidan.

Du kan prefix för vissa konfigurationskommandon med klassnamnet eller instansnamnet för motsvarande Viewer SDK-komponent. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till `setContainerId()` API-metod. Dokumentationen innehåller valfria prefix för sådana kommandon. Till exempel: `playback` dokumenteras enligt följande:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

vilket innebär att det här kommandot används på följande sätt:

* `playback` (kort syntax)
* `SmartCropVideoPlayer.playback` (kvalificerad med komponentklassnamn)
* `cont_smartCropVideoPlayer.playback` (kvalificerad med komponent-ID, förutsatt att `cont` är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Se även [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
