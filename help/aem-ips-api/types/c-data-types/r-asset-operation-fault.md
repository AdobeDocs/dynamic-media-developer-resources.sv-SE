---
description: Innehåller information om varnings- eller felförhållanden som genererats under en batchresursåtgärd. Kod- och orsaksfälten motsvarar felmeddelandefälten som skulle ha utlösts för motsvarande icke-gruppåtgärd.
seo-description: Innehåller information om varnings- eller felförhållanden som genererats under en batchresursåtgärd. Kod- och orsaksfälten motsvarar felmeddelandefälten som skulle ha utlösts för motsvarande icke-gruppåtgärd.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
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

