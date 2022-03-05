---
title: Begränsningar
description: Vissa begränsningar gäller för kapsling och inbäddning.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# Begränsningar{#restrictions}

Vissa begränsningar gäller för kapsling och inbäddning.

För bästa serverprestanda bör upplösningen för bilder som returneras av kapslade begäranden i rimlig utsträckning matcha texturupplösningen för de objekt som materialet används på.

Externa bilder cachelagras lokalt. Ändringar av sådana bilder upptäcks först när den lokala cacheposten blir inaktuell (baserat på förfallorubriken för HTTP).
