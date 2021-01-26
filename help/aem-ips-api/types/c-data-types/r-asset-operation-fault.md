---
description: Innehåller information om varnings- eller felförhållanden som genererats under en batchresursåtgärd. Kod- och orsaksfälten motsvarar felmeddelandefälten som skulle ha utlösts för motsvarande icke-gruppåtgärd.
seo-description: Innehåller information om varnings- eller felförhållanden som genererats under en batchresursåtgärd. Kod- och orsaksfälten motsvarar felmeddelandefälten som skulle ha utlösts för motsvarande icke-gruppåtgärd.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Dynamic Media Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '126'
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

