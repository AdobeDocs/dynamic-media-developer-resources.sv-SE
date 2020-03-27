---
description: Genereras när en användare inte kan autentiseras.
seo-description: Genereras när en användare inte kan autentiseras.
seo-title: authenticationFault
solution: Experience Manager
title: authenticationFault
topic: Scene7 Image Production System API
uuid: 89cc6f09-def6-4db1-a8b5-410909693dce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

