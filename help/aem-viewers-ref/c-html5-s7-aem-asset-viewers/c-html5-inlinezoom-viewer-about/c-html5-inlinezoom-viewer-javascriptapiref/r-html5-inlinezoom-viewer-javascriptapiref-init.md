---
description: JavaScript API-referens för Inline Zoom Viewer.
seo-description: JavaScript API-referens för Inline Zoom Viewer.
seo-title: init
solution: Experience Manager
title: init
uuid: a3bd0cd1-e4cb-4b09-a78f-0958b55a79e4
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Textbunden zoom
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---


# init{#init}

JavaScript API-referens för Inline Zoom Viewer.

`init()`

Startar initieringen av visningsprogrammet så att visningsprogramkoden kan hitta den med dess ID. Vid den här tidpunkten måste behållar-DOM-elementet skapas.

Om behållarelementet inte är en del av webbsideslayouten ännu (t.ex. kan det döljas med formatet `display:none` som tilldelats det), gör visningsprogrammet uppehåll i initieringsprocessen tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

Anropa endast den här metoden en gång under visningsprogrammets livscykel. efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

