---
description: Skickar ett e-postmeddelande till en angiven mottagare som svar på en cdnCacheInvalidation-åtgärd.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

Skickar ett e-postmeddelande till en angiven mottagare som svar på en cdnCacheInvalidation-åtgärd.

Syntax

## Parametrar {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Namn | Typ | Beskrivning |
|---|---|---|
| ccOriginator | `xsd:boolean` | Om värdet är true inkluderar användarens webbtjänstkonto, som är en lista över e-postmeddelanden som ska ta emot en e-postbekräftelse från Dynamic Media CDN. |
| ccOthersArray | `types:EmailArray` | En matris med e-postadresser (max 5) som ska ta emot bekräftelsemeddelandet från Dynamic Media CDN. |
