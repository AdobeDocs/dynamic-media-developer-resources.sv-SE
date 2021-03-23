---
description: Genereras när en användare inte kan autentiseras.
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 6%

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
