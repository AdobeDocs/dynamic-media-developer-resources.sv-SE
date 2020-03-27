---
description: JavaScript API-referens för Spin Viewer.
seo-description: JavaScript API-referens för Spin Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 1803028f-dcba-49da-9fb7-78bfd64fc47d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

JavaScript API-referens för Spin Viewer.

`init()`

Startar initieringen av Spin Viewer. Vid den här tidpunkten måste behållarelementet `DOM` skapas så att visningsprogramkoden kan hitta det med dess ID.

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

