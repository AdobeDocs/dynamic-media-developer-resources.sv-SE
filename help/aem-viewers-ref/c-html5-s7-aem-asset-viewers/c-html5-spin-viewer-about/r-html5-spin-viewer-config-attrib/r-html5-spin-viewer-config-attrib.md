---
title: Kommandoreferens - Konfigurationsattribut
description: Dokumentation för konfigurationsattribut för Spin Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Kommandoreferens - Konfigurationsattribut{#command-reference-configuration-attributes}

Dokumentation för konfigurationsattribut för Spin Viewer.

Alla konfigurationskommandon kan anges i URL eller med `setParam()`, eller `setParams()`, eller båda, API-metoder. Alla config-attribut kan också anges i konfigurationsposten på serversidan.

Vissa konfigurationskommandon kan ha prefixet med klassnamnet eller instansnamnet för motsvarande SDK-komponent i visningsprogrammet. Ett instansnamn för komponenten är dynamiskt och beror på ID:t för visningsbehållarens DOM-element som skickas till `setContainerId()` API-metod. Dokumentationen innehåller ett valfritt prefix för sådana kommandon. Till exempel: `zoomstep` kommandot dokumenteras enligt följande:

`[SpinView.|<containerId>_spinView].zoomstep`

Det innebär att du kan använda det här kommandot på följande sätt:

* `zoomstep` (kort syntax)
* `SpinView.zoomstep` (kvalificerad med komponentklassnamn)
* `cont_spinView.zoomstep` (kvalificerad med komponent-ID, antar `cont` är behållarelementets ID)

Se även [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
