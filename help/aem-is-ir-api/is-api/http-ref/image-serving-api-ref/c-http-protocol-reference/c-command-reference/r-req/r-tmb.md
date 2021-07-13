---
description: Miniatyrbild. Begär bilddata som är formaterade och storleksanpassade med hjälp av katalogminiatyrvillkor.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# tmb{#tmb}

Miniatyrbild. Begär bilddata som är formaterade och storleksanpassade med hjälp av katalogminiatyrvillkor.

`req=tmb`

MIME-typen för svarsdataformat och svar bestäms av `fmt=`. Stöder alla kommandon utom `fit=`.

Se [Skala för miniatyrbilder](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

HTTP-svaret kan cachas med TTL-värdet baserat på `catalog::Expiration`.
