---
description: JavaScript API-referens för Interactive Video Viewer.
seo-description: JavaScript API-referens för Interactive Video Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: e6ec0730-1ddc-4026-939c-2c9f8ecee5c7
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# init{#init}

JavaScript API-referens för Interactive Video Viewer.

`init()`

Startar initieringen av Interactive Video Viewer. Vid den här tidpunkten måste behållar-DOM-elementet skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten just nu (t.ex. kan det döljas med `display:none` ett format som tilldelats det), gör visningsprogrammet uppehåll i initieringsprocessen tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

Anropa denna metod endast en gång under tittarens livscykel. efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

