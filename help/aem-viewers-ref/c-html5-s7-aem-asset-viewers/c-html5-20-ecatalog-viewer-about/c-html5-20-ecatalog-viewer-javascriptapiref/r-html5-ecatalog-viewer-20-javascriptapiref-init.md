---
description: JavaScript API-referens för eCatalog Viewer.
seo-description: JavaScript API-referens för eCatalog Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 142381e4-aa3c-46dd-a0bd-4e090d0003e4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# init{#init}

JavaScript API-referens för eCatalog Viewer.

`init()`

Startar initieringen av eCatalog Viewer. Vid den här tidpunkten måste behållarens DOM-element skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten ännu (t.ex. kan det döljas med formatet `display:none` som tilldelats det), gör visningsprogrammet uppehåll i initieringsprocessen tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

Anropa endast den här metoden en gång under visningsprogrammets livscykel. efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```

