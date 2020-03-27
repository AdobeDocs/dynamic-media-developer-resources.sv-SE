---
description: JavaScript API-referens för eCatalog Viewer.
seo-description: JavaScript API-referens för eCatalog Viewer.
seo-title: dispose
solution: Experience Manager
title: dispose
topic: Dynamic media
uuid: 791c47e9-daab-4500-9cd0-e56ee6fc830e
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# dispose{#dispose}

JavaScript API-referens för eCatalog Viewer.

[!DNL `dispose()`]

Disponerar den här visningsprograminstansen genom att frigöra alla resurser som används av visningsprogramlogiken och ta bort alla inre objekt och komponenter som skapats av visningsprogrammet under körning.

Webbsideskoden bör även ta bort variabeln för visningsprograminstansen så att den helt tar bort visningsprogrammet från webbläsarminnet.

Om webbsideskoden har registrerade händelseavlyssnare direkt i Viewer SDK-komponenter som används av visningsprogrammet eller lagrade externa referenser till sådana komponenter, måste sådana avlyssnare uttryckligen avregistreras av webbsideskoden, och sådana externa komponentreferenser måste tas bort innan anrop [!DNL `dispose()`].

Kom inte åt visningsprogrammets API längre efter att [!DNL `dispose()`] anropas.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

