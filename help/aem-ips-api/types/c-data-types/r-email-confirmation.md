---
description: Skickar ett e-postmeddelande till en angiven mottagare som svar på en cdnCacheInvalidation-åtgärd.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# EmailConfirmation{#emailconfirmation}

Skickar ett e-postmeddelande till en angiven mottagare som svar på en cdnCacheInvalidation-åtgärd.

Syntax

## Parametrar {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Om värdet är true inkluderar användarens webbtjänstkonto, som är en lista över e-postmeddelanden som ska ta emot en e-postbekräftelse från Dynamic Media CDN. |
| `*`ccOthersArray`*` | `types:EmailArray` | En matris med e-postadresser (max 5) som ska ta emot bekräftelsemeddelanden från Dynamic Media CDN. |

