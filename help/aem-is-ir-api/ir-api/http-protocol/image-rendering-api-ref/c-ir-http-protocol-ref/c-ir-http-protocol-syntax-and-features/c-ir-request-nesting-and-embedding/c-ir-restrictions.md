---
description: Vissa begränsningar gäller för kapsling och inbäddning.
solution: Experience Manager
title: Begränsningar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# Begränsningar{#restrictions}

Vissa begränsningar gäller för kapsling och inbäddning.

För bästa serverprestanda bör upplösningen för bilder som returneras av kapslade begäranden i rimlig utsträckning matcha texturupplösningen för det eller de objekt som materialet används på.

Externa bilder cachelagras lokalt. Ändringar av sådana bilder identifieras först när den lokala cacheposten blir inaktuell (baserat på förfallorubriken för HTTP).
