---
description: Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req=img eller req=tmb.
solution: Experience Manager
title: Bilder
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# Bilder{#images}

Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req=img eller req=tmb.

MIME-typen för HTTP-svar bestäms av `fmt=`, eller om `fmt=` inte anges är det `<image/jpeg>`.

HTTP-svarsstatusen är &#39;200 OK&#39; om förfrågningsmetoden var en ovillkorlig `GET` eller `HEAD`.

Servern kan svara med statusen 304 (inte ändrad) och returnera inga bilddata som svar på en villkorlig `GET`-begäran (som innehåller en giltig `If-Modified-Since`- eller `If-None-Match`-rubrik).
