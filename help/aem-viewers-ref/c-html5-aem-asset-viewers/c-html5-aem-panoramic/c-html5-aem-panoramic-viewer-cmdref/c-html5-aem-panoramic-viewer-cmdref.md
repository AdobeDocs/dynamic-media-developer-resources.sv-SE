---
title: Kommandoreferens - Konfigurationsattribut
description: Konfigurationsattributdokumentation för panoramavisningsprogrammet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för panoramavisningsprogrammet.

Alla konfigurationskommandon kan anges i URL eller med API-metoderna `setParam()` och/eller `setParams()`. Alla config-attribut kan också anges i konfigurationsposten på serversidan.

Vissa konfigurationskommandon kan ha prefixet med klassnamnet eller instansnamnet för motsvarande HTML5 SDK-komponent. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till API-metoden `setContainerId()`. Dokumentationen innehåller ett valfritt prefix för sådana kommandon. Kommandot `vrrender` beskrivs till exempel så här:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Det innebär att det här kommandot används på följande sätt:

* `vrrender` (kort syntax)
* `PanoramicView.vrrender` (kvalificerad med komponentklassnamn)
* `cont_panoramicView.vrrender` (kvalificerad med komponent-ID, förutsatt att cont är behållarelementets ID)


Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Se [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
