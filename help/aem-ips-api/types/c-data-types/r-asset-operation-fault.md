---
description: Innehåller information om varnings- eller felförhållanden som genererats under en batchresursåtgärd. Kod- och orsaksfälten motsvarar felmeddelandefälten som skulle ha utlösts för motsvarande icke-gruppåtgärd.
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '98'
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
