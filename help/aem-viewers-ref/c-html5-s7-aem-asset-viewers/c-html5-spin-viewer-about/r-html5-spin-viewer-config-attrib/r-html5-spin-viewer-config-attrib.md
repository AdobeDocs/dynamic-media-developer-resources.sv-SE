---
description: Dokumentation för konfigurationsattribut för Spin Viewer.
seo-description: Dokumentation för konfigurationsattribut för Spin Viewer.
seo-title: Kommandoreferens - Konfigurationsattribut
solution: Experience Manager
title: Kommandoreferens - Konfigurationsattribut
topic: Dynamic media
uuid: ba60da44-d30d-459f-b3d8-5cf3ea4bcbdb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Dokumentation för konfigurationsattribut för Spin Viewer.

Alla konfigurationskommandon kan anges i URL:en eller med hjälp av API-metoderna `setParam()`, `setParams()` eller båda. Alla config-attribut kan också anges i konfigurationsposten på serversidan.

Vissa konfigurationskommandon kan ha prefixet med klassnamnet eller instansnamnet för motsvarande SDK-komponent i visningsprogrammet. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till API-metoden `setContainerId()`. Dokumentationen innehåller ett valfritt prefix för sådana kommandon. Kommandot `zoomstep` beskrivs till exempel så här:

`[SpinView.|<containerId>_spinView].zoomstep`

vilket betyder att du kan använda det här kommandot som:

* `zoomstep` (kort syntax)
* `SpinView.zoomstep` (kvalificerad med komponentklassnamn)
* `cont_spinView.zoomstep` (kvalificerad med komponent-ID, förutsatt  `cont` att är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
