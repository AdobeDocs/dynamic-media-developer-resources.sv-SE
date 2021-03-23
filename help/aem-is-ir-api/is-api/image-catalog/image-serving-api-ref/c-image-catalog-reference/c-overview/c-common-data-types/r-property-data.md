---
description: Egenskapsdata består av en textsträng som representerar en eller flera egenskaper.
seo-description: Egenskapsdata består av en textsträng som representerar en eller flera egenskaper.
seo-title: Egenskapsdata
solution: Experience Manager
title: Egenskapsdata
uuid: 7fa6ae70-8d70-41d6-9e47-7df3d616874c
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---


# Egenskapsdata{#property-data}

Egenskapsdata består av en textsträng som representerar en eller flera egenskaper.

En egenskap består av ett egenskapsnamn och ett egenskapsvärde, avgränsade med =.

Flera egenskaper avgränsas med radavgränsare, som kan vara antingen `??` eller `<CR><LF>`. Om hela egenskapsdatasträngen inte omsluts av citattecken ersätter servern varje förekomst av `??` med `<CR><LF>` innan data skickas till klienten. Egenskapsnamn kan bestå av bokstäver, siffror, &#39;.&#39;, &#39;-&#39; och &#39;_&#39;. Egenskapsnamn är inte skiftlägeskänsliga.

Egenskapsvärden får inte innehålla radavgränsare.

Se [Textsträng](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) för ytterligare regler som tillämpas på egenskapsdata.
