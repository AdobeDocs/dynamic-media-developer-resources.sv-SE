---
description: Vissa begränsningar gäller för kapsling och inbäddning.
seo-description: Vissa begränsningar gäller för kapsling och inbäddning.
seo-title: Begränsningar
solution: Experience Manager
title: Begränsningar
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Begränsningar{#restrictions}

Vissa begränsningar gäller för kapsling och inbäddning.

För bästa serverprestanda bör upplösningen för bilder som returneras av kapslade begäranden i rimlig utsträckning matcha texturupplösningen för det eller de objekt som materialet används på.

Externa bilder cachelagras lokalt. Ändringar av sådana bilder identifieras först när den lokala cacheposten blir inaktuell (baserat på förfallorubriken för HTTP).
