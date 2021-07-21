---
description: Innehåller tilläggsmeddelanden som är associerade med huvudjobbloggmeddelandet (JobDetail). Innehåller varningar och annan information som är kopplad till den aktuella bearbetade resursen.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '70'
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
