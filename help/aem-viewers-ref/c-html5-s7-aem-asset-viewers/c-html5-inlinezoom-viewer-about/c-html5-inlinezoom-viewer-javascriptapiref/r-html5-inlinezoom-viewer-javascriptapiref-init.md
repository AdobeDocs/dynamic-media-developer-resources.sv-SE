---
description: JavaScript API-referens för Inline Zoom Viewer.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Textbunden zoom
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
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
