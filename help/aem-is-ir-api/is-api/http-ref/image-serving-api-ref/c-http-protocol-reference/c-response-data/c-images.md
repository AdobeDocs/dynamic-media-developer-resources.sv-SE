---
description: Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req=img eller req=tmb.
seo-description: Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req=img eller req=tmb.
seo-title: Bilder
solution: Experience Manager
title: Bilder
topic: Scene7 Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# Bilder{#images}

Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req=img eller req=tmb.

MIME-typen för HTTP-svar bestäms av `fmt=`, eller om `fmt=` inte anges är det `<image/jpeg>`.

HTTP-svarsstatusen är &#39;200 OK&#39; om förfrågningsmetoden var en ovillkorlig `GET` eller `HEAD`.

Servern kan svara med statusen 304 (inte ändrad) och returnera inga bilddata som svar på en villkorlig `GET`-begäran (som innehåller en giltig `If-Modified-Since`- eller `If-None-Match`-rubrik).
