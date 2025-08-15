---
title: pscan
description: Progressiv JPEG-skanning. Progressiv JPEG visar en bild på ett sådant sätt att den först visar ett oskarpt/lågkvalitativt foto i sin helhet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# pscan{#pscan}

Progressiv JPEG-skanning. Progressiv JPEG visar en bild på ett sådant sätt att den först visar ett oskarpt/lågkvalitativt foto i sin helhet. När skanningen fortsätter blir den tydligare när bildens data hämtas mer fullständigt. Med den här parametern kan du ange hur många inläsningar det tar (3, 4 eller 5) för att hela bilden ska visas.

`pscan=auto|3|4|5`

Den faktiska hastigheten för varje skanning beror på överföringshastigheten för användarens system och den dator som tar emot och dekomprimerar data.

`Auto` använder skanningsinställningarna som beräknas av det oberoende JPEG-biblioteket och är beroende av färgmodellen. Värdena för `3`, `4`, `5` motsvarar den skanningsinställning som finns i Adobe Photoshop när du sparar en JPEG-fil som en pjpeg (progressiv JPEG).

Om `pscan` inte är inställt blir standardvärdet `auto`.

## Egenskaper {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Begär attribut. Används oavsett den aktuella lagerinställningen. Ignoreras om utdataformatet inte är progressivt JPEG.

## Standard {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Exempel {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Se även {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
