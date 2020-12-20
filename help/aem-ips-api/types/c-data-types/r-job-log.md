---
description: Jobbloggen när jobbet har körts.
seo-description: Jobbloggen när jobbet har körts.
seo-title: JobLog
solution: Experience Manager
title: JobLog
topic: Scene7 Image Production System API
uuid: d267009a-e4ad-4a21-ae0e-caf51d2f338b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# JobLog{#joblog}

Jobbloggen när jobbet har körts.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Företagshandtag. |
| ` *`jobHandle`*` | `xsd:string` | Jobbreferens. |
| ` *`jobName`*` | `xsd:string` | Jobbnamn. |
| ` *`originalJobName`*` | `xsd:string` | Det ursprungliga namnet som skickades för jobbet med `submitJob`. |
| ` *`submitUserEmail`*` | `xsd:string` | E-postadressen till den användare som skickade jobbet. |
| ` *`logType`*` | `xsd:string` | Val av jobbloggtyper. |
| ` *`jobSubType`*` | `xsd:string` | Ytterligare jobbinformation. |
| ` *`startDate`*` | `xsd:dateTime` | Startdatum, tid och tidszon för jobbet. |
| ` *`endDate`*` | `xsd:dateTime` | Jobbets slutdatum, tid och tidszon. |
| ` *`description`*` | `xsd:string` | En beskrivning av jobbet som ursprungligen angavs i `submitJob`. |
| ` *`fileSuccessCount`*` | `xsd:int` | Antal filer som bearbetats. |
| ` *`fileErrorCount`*` | `xsd:int` | Antal filer som orsakade ett fel. |
| ` *`fileWarningCount`*` | `xsd:int` | Antal filer som genererade en varning. |
| ` *`fileDuplicateCount`*` | `xsd:int` | Antal duplicerade filer. |
| ` *`fileUpdateCount`*` | `xsd:int` | Antal uppdaterade filer. |
| ` *`totalFileCount`*` | `xsd:int` | Antal filer som bearbetats av det loggade jobbet. |
| ` *`transferSuccessCount`*` | `xsd:int` | Antal slutförda överföringar. |
| ` *`transferErrorCount`*` | `xsd:int` | Antal överföringsfel. |
| ` *`transferWarningCount`*` | `xsd:int` | Antal överföringsvarningar. |
| ` *`fatalError`*` | `xsd:boolean` | Anger om jobbet genererade ett allvarligt fel. |
| ` *`detailTotalRows`*` | `xsd:int` | Det totala antalet rader som matchar frågan, som kan vara större än storleken på `detailArray` på grund av sidstorleksbegränsningar. |
| ` *`detailArray`*` | `types:JobLogDetailArray` | Arrayen med information om det loggade jobbet. |

