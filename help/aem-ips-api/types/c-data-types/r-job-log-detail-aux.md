---
description: Innehåller tilläggsmeddelanden som är associerade med huvudjobbloggmeddelandet (JobDetail). Innehåller varningar och annan information som är kopplad till den aktuella bearbetade resursen.
seo-description: Innehåller tilläggsmeddelanden som är associerade med huvudjobbloggmeddelandet (JobDetail). Innehåller varningar och annan information som är kopplad till den aktuella bearbetade resursen.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# JobLogDetailAux{#joblogdetailaux}

Innehåller tilläggsmeddelanden som är associerade med huvudjobbloggmeddelandet (JobDetail). Innehåller varningar och annan information som är kopplad till den aktuella bearbetade resursen.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Ett hjälpmeddelande. |
| `*`logType`*` | `xsd:string` | Loggtyp: `IPSJobLog.gcUploadWarning` eller `IPSJobLog.gcUploadError`. |
| `*`dateCreated`*` | `xsd:dateTime` | Datum när hjälpjobbloggen skapades. |

