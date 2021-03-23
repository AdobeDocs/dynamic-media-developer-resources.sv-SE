---
description: JavaScript API-referens för Basic Zoom Viewer.
seo-description: JavaScript API-referens för Basic Zoom Viewer.
seo-title: dispose
solution: Experience Manager
title: dispose
uuid: 6c1af089-37f0-4e1f-9e62-68a70df1a0f0
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Zoom
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# dispose{#dispose}

JavaScript API-referens för Basic Zoom Viewer.

`dispose()`

Disponerar den här visningsprograminstansen genom att frigöra alla resurser som används av visningsprogramlogiken och ta bort alla inre objekt och komponenter som skapats av visningsprogrammet under körning.

Webbsideskoden bör även ta bort variabeln för visningsprograminstansen så att den helt tar bort visningsprogrammet från webbläsarminnet.

Om webbsideskoden har registrerade händelseavlyssnare direkt i Viewer SDK-komponenter som används av visningsprogrammet eller lagrade externa referenser till sådana komponenter måste sådana avlyssnare uttryckligen avregistreras av webbsideskoden, och sådana externa komponentreferenser måste tas bort innan du anropar `dispose()`.

Åtkomst inte till visningsprogrammets API längre efter att `dispose()` har anropats.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

