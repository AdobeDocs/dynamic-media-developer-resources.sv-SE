---
description: Egenskapsdata består av en textsträng som representerar en eller flera egenskaper.
solution: Experience Manager
title: Egenskapsdata
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Egenskapsdata{#property-data}

Egenskapsdata består av en textsträng som representerar en eller flera egenskaper.

En egenskap består av ett egenskapsnamn och ett egenskapsvärde, avgränsade med =.

Flera egenskaper avgränsas med radavgränsare, som kan vara antingen `??` eller `<CR><LF>`. Om hela egenskapsdatasträngen inte omsluts av citattecken ersätter servern varje förekomst av `??` med `<CR><LF>` innan data skickas till klienten. Egenskapsnamn kan bestå av bokstäver, siffror, &#39;.&#39;, &#39;-&#39; och &#39;_&#39;. Egenskapsnamn är inte skiftlägeskänsliga.

Egenskapsvärden får inte innehålla radavgränsare.

Se [Textsträng](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) för ytterligare regler som tillämpas på egenskapsdata.
