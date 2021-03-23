---
description: JavaScript API-referens för visningsprogrammet för utfällbara bilder.
seo-description: JavaScript API-referens för visningsprogrammet för utfällbara bilder.
seo-title: init
solution: Experience Manager
title: init
uuid: e5d990af-1c5a-4253-8ecd-b51119cee3a2
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Flyout
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# init{#init}

JavaScript API-referens för visningsprogrammet för utfällbara bilder.

`init()`

Startar initieringen av visningsprogrammet. Vid den här tidpunkten måste behållar-DOM-elementet skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten ännu (t.ex. kan det döljas med formatet `display:none` som tilldelats det), gör visningsprogrammet uppehåll i initieringsprocessen tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

Den här metoden ska bara anropas en gång under visningsprogrammets livscykel, efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

