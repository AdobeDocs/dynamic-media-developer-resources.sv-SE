---
description: Miniatyrbild. Begär bilddata som är formaterade och storleksanpassade med hjälp av katalogminiatyrvillkor.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---


# tmb{#tmb}

Miniatyrbild. Begär bilddata som är formaterade och storleksanpassade med hjälp av katalogminiatyrvillkor.

`req=tmb`

MIME-typen för svarsdataformat och svar bestäms av `fmt=`. Stöder alla kommandon utom `fit=`.

Se [Skala för miniatyrbilder](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

HTTP-svaret kan cachas med TTL-värdet baserat på `catalog::Expiration`.
