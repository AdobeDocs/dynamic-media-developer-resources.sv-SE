---
title: AssetContextStateUpdate
description: Ange en ny uppsättning flaggor för publiceringsläge för den publiceringskontext som är kopplad till en resurs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

Ange en ny uppsättning flaggor för publiceringsläge för den publiceringskontext som är kopplad till en resurs.

**Parametrar**

| Namn | Typ | Beskrivning |
|---|---|---|
| assetHandle | `xsd:string` | Hantera resursen som du vill uppdatera. |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | En array med kontaktlägen för publicering för resursen som du vill uppdatera. |
