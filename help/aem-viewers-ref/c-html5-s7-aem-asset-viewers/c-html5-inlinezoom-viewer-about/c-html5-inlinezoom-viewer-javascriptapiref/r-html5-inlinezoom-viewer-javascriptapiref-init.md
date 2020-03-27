---
description: JavaScript API-referens för Inline Zoom Viewer.
seo-description: JavaScript API-referens för Inline Zoom Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: a3bd0cd1-e4cb-4b09-a78f-0958b55a79e4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

JavaScript API-referens för Inline Zoom Viewer.

`init()`

Startar initieringen av visningsprogrammet så att visningsprogramkoden kan hitta den med dess ID. Vid den här tidpunkten måste behållar-DOM-elementet skapas.

Om behållarelementet inte är en del av webbsideslayouten just nu (t.ex. kan det döljas med `display:none` ett format som tilldelats det), gör visningsprogrammet uppehåll i initieringsprocessen tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

Anropa endast den här metoden en gång under visningsprogrammets livscykel. efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

