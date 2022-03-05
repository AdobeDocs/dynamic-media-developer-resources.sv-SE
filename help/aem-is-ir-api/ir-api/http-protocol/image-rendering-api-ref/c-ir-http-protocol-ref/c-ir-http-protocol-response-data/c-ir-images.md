---
title: Bilder
description: Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req= har något av följande värden img, felsök.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Bilder{#images}

Bilddata returneras om en begäran har slutförts och om begäran antingen inte innehåller ett req=-kommando eller om req= har något av följande värden: img, debug

MIME-typen för HTTP-svar bestäms av `fmt=`, eller om `fmt=` har inte angetts, beror på värdet för `attribute::Format`.

HTTP-svarsstatusen är &quot;200 OK&quot; om förfrågningsmetoden var ovillkorlig `GET` eller `HEAD`.

Servern kan svara med statusen 304 (inte ändrad) och returnera inga bilddata som svar på ett villkorligt `GET` begäran (med [!DNL If-Modified-Since] fältet finns i `request-header`).
