---
description: Vissa begränsningar gäller för kapsling och inbäddning.
solution: Experience Manager
title: Begränsningar
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Begränsningar{#restrictions}

Vissa begränsningar gäller för kapsling och inbäddning.

För bästa serverprestanda bör upplösningen för bilder som returneras av kapslade begäranden i rimlig utsträckning matcha texturupplösningen för det eller de objekt som materialet används på.

Externa bilder cachelagras lokalt. Ändringar av sådana bilder identifieras först när den lokala cacheposten blir inaktuell (baserat på förfallorubriken för HTTP).
