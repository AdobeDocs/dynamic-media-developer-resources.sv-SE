---
description: JavaScript API-referens för visningsprogrammet för smart beskärning.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: d46a9c8b-064a-4928-b30e-885b12d287ab
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# init{#init}

JavaScript API-referens för visningsprogrammet för smart beskärning.

`init()`

Startar initieringen av videovisningsprogrammet för smart beskärning. Vid den här tidpunkten måste behållar-DOM-elementet skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten ännu, till exempel, kan det vara dolt med `display:none` det format som tilldelats det - visningsprogrammet avbryter sin initieringsprocess tills den tidpunkt då webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

Anropa denna metod endast en gång under tittarens livscykel. efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
