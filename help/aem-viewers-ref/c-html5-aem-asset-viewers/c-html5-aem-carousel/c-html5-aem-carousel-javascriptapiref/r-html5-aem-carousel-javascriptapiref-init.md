---
title: init
description: JavaScript API-referens för Carousel Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 00e09e26-1380-487c-9512-34d805f1330d
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# init{#init}

JavaScript API-referens för Carousel Viewer.

`init()`

Startar initieringen av Carousel Viewer. Vid den här tidpunkten måste behållar-DOM-elementet skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten än, kan det till exempel döljas med `display:none` style - visningsprogrammet avbryter initieringsprocessen. Den pausas tills webbsidan återför behållarelementet till layouten, då visningsprogrammet automatiskt laddas igen.

Anropa denna metod endast en gång under tittarens livscykel. efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
