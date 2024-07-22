---
title: init
description: JavaScript API-referens för Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# init{#init}

JavaScript API-referens för Video360 Viewer.

`init()`

Startar initieringen av Video360 Viewer. Vid den här tidpunkten måste behållar-DOM-elementet skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten än (t.ex. kan det döljas med formatet `display:none` som tilldelats det) gör visningsprogrammet uppehåll i initieringsprocessen. Det gör det tills webbsidan återför behållarelementet till layouten. När den här händelsen inträffar återtas visningsprogrammet automatiskt.

Anropa den här metoden endast en gång under visningsprogrammets livscykel. Efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
