---
description: JavaScript API-referens för eCatalog Viewer.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# init{#init}

JavaScript API-referens för eCatalog Viewer.

[!DNL `init()`]

Startar initieringen av eCatalog Viewer. Vid den här tidpunkten måste behållarens DOM-element skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten ännu (t.ex. kan det döljas med [!DNL `display:none`] det format som har tilldelats) gör visningsprogrammet uppehåll i initieringsprocessen tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

Anropa endast den här metoden en gång under visningsprogrammets livscykel. efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
