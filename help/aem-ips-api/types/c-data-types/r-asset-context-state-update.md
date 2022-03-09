---
title: AssetContextStateUpdate
description: Ange en ny uppsättning flaggor för publiceringsläge för den publiceringskontext som är kopplad till en resurs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---

# AssetContextStateUpdate{#assetcontextstateupdate}

Ange en ny uppsättning flaggor för publiceringsläge för den publiceringskontext som är kopplad till en resurs.

**Parametrar**

| Namn | Typ | Beskrivning |
|---|---|---|
| assetHandle | `xsd:string` | Hantera resursen som du vill uppdatera. |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | En array med kontaktlägen för publicering för resursen som du vill uppdatera. |
