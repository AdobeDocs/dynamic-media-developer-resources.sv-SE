---
description: Innehåller information om varnings- eller felförhållanden som genererats under en batchresursåtgärd. Kod- och orsaksfälten motsvarar felmeddelandefälten som skulle ha utlösts för motsvarande icke-gruppåtgärd.
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# AssetOperationFault{#assetoperationfault}

Innehåller information om varnings- eller felförhållanden som genererats under en batchresursåtgärd. Kod- och orsaksfälten motsvarar felmeddelandefälten som skulle ha utlösts för motsvarande icke-gruppåtgärd.

Syntax

## Parametrar {#section-c906f052f43e4785ba46d92b514b0923}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Resurshandtag för den misslyckade åtgärden. |
| `*`kod`*` | `xsd:int` | Felkod för åtgärd. |
| `*`orsak`*` | `xsd:string` | Felbeskrivning eller orsak. |

