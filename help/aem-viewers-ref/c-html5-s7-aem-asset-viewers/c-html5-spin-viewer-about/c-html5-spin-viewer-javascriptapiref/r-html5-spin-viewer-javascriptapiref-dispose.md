---
title: dispose
description: JavaScript API-referens för Spin Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: c19466a8-9fc5-440c-8bb1-c4528937a522
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# dispose{#dispose}

JavaScript API-referens för Spin Viewer.

`dispose()`

Disponerar den här visningsprograminstansen genom att frigöra alla resurser som används av visningsprogramlogiken och ta bort alla inre objekt och komponenter som skapats av visningsprogrammet under körning.

Webbsideskoden bör även ta bort variabeln för visningsprograminstansen så att den helt tar bort visningsprogrammet från webbläsarminnet.

Om webbsideskoden har registrerade händelseavlyssnare direkt i Viewer SDK-komponenter som används av visningsprogrammet - eller lagrade externa referenser till sådana komponenter - måste sådana avlyssnare uttryckligen avregistreras av webbsideskoden. Sådana externa komponentreferenser måste tas bort innan `dispose()` anropas.

Åtkomst inte längre till visningsprogrammets API efter att `dispose()` har anropats.

## Parametrar {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ingen.

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
