---
description: Vissa begränsningar gäller för kapsling och inbäddning.
seo-description: Vissa begränsningar gäller för kapsling och inbäddning.
seo-title: Begränsningar
solution: Experience Manager
title: Begränsningar
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Begränsningar{#restrictions}

Vissa begränsningar gäller för kapsling och inbäddning.

För bästa serverprestanda bör upplösningen för bilder som returneras av kapslade begäranden i rimlig utsträckning matcha texturupplösningen för det eller de objekt som materialet används på.

Externa bilder cachelagras lokalt. Ändringar av sådana bilder identifieras först när den lokala cacheposten blir inaktuell (baserat på förfallorubriken för HTTP).
