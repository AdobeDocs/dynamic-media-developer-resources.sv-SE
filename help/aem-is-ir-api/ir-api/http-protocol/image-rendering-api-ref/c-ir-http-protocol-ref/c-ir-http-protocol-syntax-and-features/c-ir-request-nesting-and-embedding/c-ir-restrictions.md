---
description: Vissa begränsningar gäller för kapsling och inbäddning.
solution: Experience Manager
title: Begränsningar
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Begränsningar{#restrictions}

Vissa begränsningar gäller för kapsling och inbäddning.

För bästa serverprestanda bör upplösningen för bilder som returneras av kapslade begäranden i rimlig utsträckning matcha texturupplösningen för det eller de objekt som materialet används på.

Externa bilder cachelagras lokalt. Ändringar av sådana bilder identifieras först när den lokala cacheposten blir inaktuell (baserat på förfallorubriken för HTTP).
