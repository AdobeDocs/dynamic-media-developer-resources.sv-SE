---
title: dispose
description: JavaScript API-referens för Video Image Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 8af8506e-6b29-45ea-a70b-3eb3b2995047
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# dispose{#dispose}

JavaScript API-referens för Video Image Viewer.

`dispose()`

Disponerar den här visningsprograminstansen genom att frigöra alla resurser som används av visningsprogramlogiken och ta bort alla inre objekt och komponenter som skapats av visningsprogrammet under körning.

Webbsideskoden bör även ta bort variabeln för visningsprograminstansen så att den helt tar bort visningsprogrammet från webbläsarminnet.

Om webbsideskoden har registrerade händelseavlyssnare direkt i Viewer SDK-komponenter som används av visningsprogrammet - eller lagrade externa referenser till sådana komponenter - måste sådana avlyssnare uttryckligen avregistreras av webbsideskoden. Sådana externa komponentreferenser måste tas bort innan anrop görs `dispose()`.

Åtkomst inte längre till visningsprogrammets API efter `dispose()` anropas.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
