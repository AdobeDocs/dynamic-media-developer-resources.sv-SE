---
description: Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req= har något av följande värden img, felsök
seo-description: Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req= har något av följande värden img, felsök
seo-title: Bilder
solution: Experience Manager
title: Bilder
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Bilder{#images}

Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req= har något av följande värden: img, debug

MIME-typen för HTTP-svar bestäms av `fmt=`, eller, om `fmt=` inte anges, beror det på värdet `attribute::Format`.

HTTP-svarsstatusen är &#39;200 OK&#39; om förfrågningsmetoden var en ovillkorlig `GET` eller `HEAD`.

Servern kan svara med statusen 304 (inte ändrad) och returnera inga bilddata som svar på en villkorlig `GET`-begäran (med fältet [!DNL If-Modified-Since] i `request-header`).
