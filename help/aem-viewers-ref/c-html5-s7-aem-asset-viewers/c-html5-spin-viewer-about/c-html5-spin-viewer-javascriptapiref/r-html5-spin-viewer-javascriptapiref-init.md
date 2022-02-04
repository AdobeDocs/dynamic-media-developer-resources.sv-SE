---
title: init
description: JavaScript API-referens för Spin Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# init{#init}

JavaScript API-referens för Spin Viewer.

`init()`

Startar initieringen av Spin Viewer. Vid den här tidpunkten `DOM` måste skapas så att visningsprogramkoden kan hitta det med dess ID.

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
