---
title: init
description: JavaScript API-referens för initiering av visningsprogrammet för utfällbara menyer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# init{#init}

JavaScript API-referens för visningsprogrammet.

`init()`

Startar initieringen av visningsprogrammet. Vid den här tidpunkten måste behållar-DOM-elementet skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet ännu inte är en del av webbsidans layout kan det döljas med formatet `display:none` som tilldelats det - visningsprogrammet avbryter initieringsprocessen. Det gör det tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

Den här metoden ska bara anropas en gång under visningsprogrammets livscykel, efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
