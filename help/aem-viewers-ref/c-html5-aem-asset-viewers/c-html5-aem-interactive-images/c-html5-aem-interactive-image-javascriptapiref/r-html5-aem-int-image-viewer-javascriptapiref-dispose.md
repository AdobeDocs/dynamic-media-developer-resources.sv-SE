---
description: JavaScript API-referens för Video Image Viewer.
solution: Experience Manager
title: dispose
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva bilder
role: Utvecklare,Affärsledare
exl-id: 8af8506e-6b29-45ea-a70b-3eb3b2995047
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# dispose{#dispose}

JavaScript API-referens för Video Image Viewer.

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
