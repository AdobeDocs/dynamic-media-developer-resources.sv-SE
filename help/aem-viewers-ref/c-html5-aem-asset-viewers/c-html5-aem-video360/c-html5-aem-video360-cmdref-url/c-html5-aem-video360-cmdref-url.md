---
description: Kommandoreferensdokumentation för Video360 Viewer.
seo-description: Kommandoreferensdokumentation för Video360 Viewer.
seo-title: Kommandoreferens - URL
solution: Experience Manager
title: Kommandoreferens - URL
uuid: 70c212d7-35ee-408f-abe4-19ba1e4d773d
feature: Dynamic Media Classic,visningsprogram,SDK/API,360 VR-video
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# Kommandoreferens - URL{#command-reference-url}

Kommandoreferensdokumentation för Video360 Viewer.

Du kan ange valfritt konfigurationskommando i URL:en. Du kan också använda API-metoderna `setParam()`, `setParams()` eller båda för att ange ett konfigurationskommando. Du kan också ange valfritt config-attribut i konfigurationsposten på serversidan.

Du kan prefix för vissa konfigurationskommandon med klassnamnet eller instansnamnet för motsvarande HTML5 Viewer SDK-komponent. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till API-metoden `setContainerId()`. Dokumentationen innehåller valfria prefix för sådana kommandon. `playback` dokumenteras till exempel enligt följande:

```
[Video360Player.|<containerId>_video360Player].playback
```

vilket innebär att det här kommandot används på följande sätt:

* `playback` (kort syntax)
* `Video360Player.playback` (kvalificerad med komponentklassnamn)
* `cont_video360Player.playback` (kvalificerad med komponent-ID, förutsatt att det  `cont` är behållarelementets ID)

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
