---
description: Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req= har något av följande värden img, felsök.
solution: Experience Manager
title: Bilder
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# Bilder{#images}

Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req= har något av följande värden: img, debug

MIME-typen för HTTP-svar bestäms av `fmt=`, eller, om `fmt=` inte anges, beror det på värdet `attribute::Format`.

HTTP-svarsstatusen är &#39;200 OK&#39; om förfrågningsmetoden var en ovillkorlig `GET` eller `HEAD`.

Servern kan svara med statusen 304 (inte ändrad) och returnera inga bilddata som svar på en villkorlig `GET`-begäran (med fältet [!DNL If-Modified-Since] i `request-header`).
