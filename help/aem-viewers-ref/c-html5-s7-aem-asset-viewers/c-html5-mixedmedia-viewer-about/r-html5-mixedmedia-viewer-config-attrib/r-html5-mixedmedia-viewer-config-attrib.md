---
description: Konfigurationsattributdokumentation för blandad mediavisare.
seo-description: Konfigurationsattributdokumentation för blandad mediavisare.
seo-title: Kommandoreferens - Konfigurationsattribut
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
topic: Dynamic Media
uuid: c0f09a05-f024-4cf0-a65f-0bfee015f635
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Konfigurationsattributdokumentation för blandad mediavisare.

Alla konfigurationskommandon kan anges i URL:en eller med hjälp av API-metoderna `setParam()`, `setParams()` eller båda. Alla config-attribut kan också anges i konfigurationsposten på serversidan.

Vissa konfigurationskommandon kan ha prefixet med klassnamnet eller instansnamnet för motsvarande SDK-komponent i visningsprogrammet. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till API-metoden `setContainerId()`. Dokumentationen innehåller ett valfritt prefix för sådana kommandon. Kommandot `zoomstep` beskrivs till exempel så här:

`[ZoomView.|<containerId>_zoomView].zoomstep`

vilket betyder att du kan använda det här kommandot som:

* `zoomstep` (kort syntax)
* `ZoomView.zoomstep` (kvalificerad med komponentklassnamn)
* `cont_zoomView.zoomstep` (kvalificerad med komponent-ID, förutsatt  `cont` att är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
