---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 12%

---


# ipsApiFault{#ipsapifault}

Syntax

## Feltyper {#section-425697675cac4b2ab5c48bd463956401}

| ID | Fel |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## Felfält {#section-37fe1aef1d5f4ca480071ca933aba826}

| Namn | Typ | Beskrivning |
|---|---|---|
| `code` | `xsd:int` | Fel-ID |
| `reason` | `xsd:string` | Ett informativt meddelande som beskriver felet. |

