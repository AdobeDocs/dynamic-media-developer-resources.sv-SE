---
description: Genereras när en användare inte kan autentiseras.
solution: Experience Manager
title: authenticationFault
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 8%

---


# authenticationFault{#authenticationfault}

Genereras när en användare inte kan autentiseras.

Syntax

## Feltyper {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | Fel |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## Felfält {#section-1fe84846a7154b03ab49552810ee9ac3}

| Namn | Typ | Beskrivning |
|---|---|---|
| `code` | `xsd:int` | Fel-ID |
| `reason` | `xsd:string` | Ett informativt meddelande som beskriver felet. |
