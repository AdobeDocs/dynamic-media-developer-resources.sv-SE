---
title: dispose
description: JavaScript API-referens för panoramavisningsprogrammet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 4e6ad465-36df-49e2-8c9e-722e8aa9063e
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# dispose{#dispose}

JavaScript API-referens för panoramavisningsprogrammet.

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
