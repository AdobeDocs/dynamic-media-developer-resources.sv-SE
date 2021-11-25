---
title: init
description: JavaScript API-referens för panoramavisningsprogrammet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# init{#init}

JavaScript API-referens för panoramavisningsprogrammet.

`init()`

Startar initieringen av panoramavisningsprogrammet. Vid den här tidpunkten måste behållar-DOM-elementet skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten än (t.ex. kan det döljas med `display:none` format som tilldelats), kommer visningsprogrammet att avbryta sin initieringsprocess. Det gör det tills webbsidan återför behållarelementet till layouten. När den här händelsen inträffar återtas visningsprogrammet automatiskt.

Den här metoden ska bara anropas en gång under visningsprogrammets livscykel, efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
