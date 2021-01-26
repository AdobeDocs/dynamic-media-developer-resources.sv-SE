---
description: Innehåller tilläggsmeddelanden som är associerade med huvudjobbloggmeddelandet (JobDetail). Innehåller varningar och annan information som är kopplad till den aktuella bearbetade resursen.
seo-description: Innehåller tilläggsmeddelanden som är associerade med huvudjobbloggmeddelandet (JobDetail). Innehåller varningar och annan information som är kopplad till den aktuella bearbetade resursen.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
topic: Dynamic Media Image Production System API
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '88'
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

