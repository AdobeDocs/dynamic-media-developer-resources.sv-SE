---
title: init
description: JavaScript API-referens för eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# init{#init}

JavaScript API-referens för eCatalog Viewer.

[!DNL `init()`]

Startar initieringen av eCatalog Viewer. Nu måste behållar-DOM-elementet skapas så att visningsprogramkoden kan hitta det med dess ID.

Om behållarelementet inte är en del av webbsideslayouten än, till exempel om det är dolt med formatet [!DNL `display:none`] som tilldelats det, kommer visningsprogrammet att avbryta initieringsprocessen. Det gör det tills webbsidan återför behållarelementet till layouten. När den här händelsen inträffar återtas visningsprogrammet automatiskt.

Anropa bara den här metoden en gång under visningsprogrammets livscykel. Efterföljande anrop ignoreras.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] En referens till visningsprograminstansen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
