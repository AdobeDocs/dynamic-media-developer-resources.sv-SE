---
title: init
description: JavaScript API-referens för visningsprogrammet för smart beskärning.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: e197c4dd-346d-4ef4-beb7-cbd0049dff05
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# init{#init}

JavaScript API-referens för visningsprogrammet för smart beskärning.

`init()`

Startar initieringen av videovisningsprogrammet för smart beskärning. Vid den här tidpunkten måste behållar-DOM-elementet skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten än, kan det till exempel döljas med `display:none` format som tilldelats det - visningsprogrammet avbryter sin initieringsprocess. Det gör det tills webbsidan återför behållarelementet till layouten. När den här åtgärden utförs återtas visningsprogrammet automatiskt.

Anropa denna metod endast en gång under tittarens livscykel. efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
