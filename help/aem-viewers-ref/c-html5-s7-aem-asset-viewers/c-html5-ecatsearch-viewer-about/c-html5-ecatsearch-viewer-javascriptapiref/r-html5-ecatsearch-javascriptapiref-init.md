---
description: JavaScript API-referens för eCatalog Viewer.
seo-description: JavaScript API-referens för eCatalog Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: b01f1497-8bee-4e01-8f92-272b324cb2dd
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# init{#init}

JavaScript API-referens för eCatalog Viewer.

[!DNL `init()`]

Startar initieringen av eCatalog Viewer. Vid den här tidpunkten måste behållarens DOM-element skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten ännu (t.ex. kan det döljas med formatet [!DNL `display:none`] som tilldelats det), gör visningsprogrammet uppehåll i initieringsprocessen tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

Anropa endast den här metoden en gång under visningsprogrammets livscykel. efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

