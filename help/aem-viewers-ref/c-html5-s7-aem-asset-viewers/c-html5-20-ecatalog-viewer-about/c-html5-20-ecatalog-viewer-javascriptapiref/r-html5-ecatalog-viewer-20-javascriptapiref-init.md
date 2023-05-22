---
title: init
description: JavaScript API-referens för eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e7775a65-67bf-4ad6-8e51-1fdf141946bc
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# init{#init}

JavaScript API-referens för eCatalog Viewer.

`init()`

Startar initieringen av eCatalog Viewer. Vid den här tidpunkten måste behållarens DOM-element skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten än, kan det till exempel döljas med `display:none` format som tilldelats det - visningsprogrammet avbryter sin initieringsprocess. Det gör det tills webbsidan återför behållarelementet till layouten. När den här åtgärden utförs återtas visningsprogrammet automatiskt.

Anropa endast den här metoden en gång under visningsprogrammets livscykel. efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```
