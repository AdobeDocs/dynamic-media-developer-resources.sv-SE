---
description: Egenskapsdata består av en textsträng som representerar en eller flera egenskaper.
solution: Experience Manager
title: Egenskapsdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# Egenskapsdata{#property-data}

Egenskapsdata består av en textsträng som representerar en eller flera egenskaper.

En egenskap består av ett egenskapsnamn och ett egenskapsvärde, avgränsade med =.

Flera egenskaper avgränsas med radavgränsare, som kan vara antingen `??` eller `<CR><LF>`. Om hela egenskapsdatasträngen inte omsluts av citattecken ersätter servern varje förekomst av `??` med `<CR><LF>` innan data skickas till klienten. Egenskapsnamn kan bestå av bokstäver, siffror, &#39;.&#39;, &#39;-&#39; och &#39;_&#39;. Egenskapsnamnen är inte skiftlägeskänsliga.

Egenskapsvärden får inte innehålla radavgränsare.

Se [Textsträng](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) om du vill ha ytterligare regler för egenskapsdata.
