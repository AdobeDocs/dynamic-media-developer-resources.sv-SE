---
title: AssetOperationFault
description: Innehåller information om varnings- eller felförhållanden som genererats under en batchresursåtgärd. Kod- och orsaksfälten motsvarar felmeddelandefälten som skulle ha utlösts för motsvarande icke-gruppåtgärd.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# AssetOperationFault{#assetoperationfault}

Innehåller information om varnings- eller felförhållanden som genererats under en batchresursåtgärd. Kod- och orsaksfälten motsvarar felmeddelandefälten som skulle ha utlösts för motsvarande icke-gruppåtgärd.

Syntax

## Parametrar {#section-c906f052f43e4785ba46d92b514b0923}

| Namn | Typ | Beskrivning |
|---|---|---|
| assetHandle | `xsd:string` | Resurshandtag för den misslyckade åtgärden. |
| kod | `xsd:int` | Felkod för åtgärd. |
| orsak | `xsd:string` | Felbeskrivning eller orsak. |
