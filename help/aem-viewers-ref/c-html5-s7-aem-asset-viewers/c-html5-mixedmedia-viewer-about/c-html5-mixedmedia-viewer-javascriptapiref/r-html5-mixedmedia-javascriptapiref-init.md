---
title: init
description: JavaScript API-referens för visningsprogrammet för blandade media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4fb40cec-172a-41b3-98fc-927da88c7cb9
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# init{#init}

JavaScript API-referens för visningsprogrammet för blandade media.

`init()`

Startar initieringen av visningsprogrammet för blandade media. Vid den här tidpunkten måste behållar-DOM-elementet skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten än - till exempel kan det vara dolt med formatet `display:none` - gör visningsprogrammet uppehåll i initieringsprocessen. Den pausas tills webbsidan återför behållarelementet till layouten, då visningsprogrammet automatiskt laddas igen.

Anropa bara den här metoden en gång under visningsprogrammets livscykel. Efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
