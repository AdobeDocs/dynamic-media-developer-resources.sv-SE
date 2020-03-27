---
description: Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req= har något av följande värden img, felsök
seo-description: Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req= har något av följande värden img, felsök
seo-title: Bilder
solution: Experience Manager
title: Bilder
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Bilder{#images}

Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req= har något av följande värden: img, debug

MIME-typen för HTTP-svar bestäms av `fmt=`, eller, om `fmt=` inte anges, beror det på värdet för `attribute::Format`.

HTTP-svarsstatusen är &quot;200 OK&quot; om förfrågningsmetoden var ovillkorlig `GET` eller `HEAD`.

Servern kan svara med statusen 304 (inte ändrad) och returnera inga bilddata som svar på en villkorlig `GET` begäran (med [!DNL If-Modified-Since] fältet i `request-header`).
