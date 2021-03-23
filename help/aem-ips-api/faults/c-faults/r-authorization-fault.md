---
description: Genereras när en autentiserad användare inte har tillräcklig behörighet för att utföra en uppgift.
solution: Experience Manager
title: permissionFault
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 16%

---


# authenticationFault{#authorizationfault}

Genereras när en autentiserad användare inte har tillräcklig behörighet för att utföra en uppgift.

Syntax

## Feltyper {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | Fel |
|---|---|
| 20000 | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY` |
| 20001 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME` |
| 20002 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER` |
| 20003 | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION` |
| 20004 | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION` |
| 20005 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE` |
| 20006 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY` |
| 20007 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER` |
| 20008 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP` |
| 20009 | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION` |

## Felfält {#section-4e3e41f41fea402a9ae314bfd05f663e}

| Namn | Typ | Beskrivning |
|---|---|---|
| `code` | `xsd:int` | Fel-ID |
| `reason` | `xsd:string` | Ett informativt meddelande som beskriver felet. |

