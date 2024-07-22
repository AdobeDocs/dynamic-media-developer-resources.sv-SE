---
description: Assets som tillhör en bilduppsättning.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---

# [!DNL ImageSetMember]{#imagesetmember}

Assets som tillhör en bilduppsättning.

Sidåterställning innebär att en [!DNL eCatalog] ska starta en ny sida. `RenderSet` anger att den ingår i en `RenderSet`-färgruta. Värdet tvingas till `true` för `eCatalog`- och `RenderSet`-uppsättningar.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| resurs | `type:Asset` | Assets i bilduppsättningsarrayen. |
| pageReset | `xsd:boolean` | Startar en ny sida. Inställningen ignoreras och värdet tvingas till `true` för `eCatalog`- och `RenderSet`-uppsättningar. |
