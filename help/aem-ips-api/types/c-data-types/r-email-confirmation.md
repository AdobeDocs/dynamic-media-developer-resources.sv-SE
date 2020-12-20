---
description: Skickar ett e-postmeddelande till en angiven mottagare som svar på en cdnCacheInvalidation-åtgärd.
seo-description: Skickar ett e-postmeddelande till en angiven mottagare som svar på en cdnCacheInvalidation-åtgärd.
seo-title: EmailConfirmation
solution: Experience Manager
title: EmailConfirmation
topic: Scene7 Image Production System API
uuid: c3b7aada-a03a-418d-80b2-31a86a1af786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# EmailConfirmation{#emailconfirmation}

Skickar ett e-postmeddelande till en angiven mottagare som svar på en cdnCacheInvalidation-åtgärd.

Syntax

## Parametrar {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Namn | Typ | Beskrivning |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | Om värdet är true inkluderar användarens webbtjänstkonto, som är en lista över e-postmeddelanden som ska ta emot en e-postbekräftelse från Scene7 CDN. |
| ` *`ccOthersArray`*` | `types:EmailArray` | En matris med e-postadresser (max 5) som ska ta emot bekräftelsemeddelanden från Scene7 CDN. |

