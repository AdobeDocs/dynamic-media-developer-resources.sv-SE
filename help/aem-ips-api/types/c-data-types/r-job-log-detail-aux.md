---
description: Innehåller tilläggsmeddelanden som är associerade med huvudjobbloggmeddelandet (JobDetail). Innehåller varningar och annan information som är kopplad till den aktuella bearbetade resursen.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '72'
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

