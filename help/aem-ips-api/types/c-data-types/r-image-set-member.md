---
description: Resurser som tillhör en bilduppsättning.
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

Resurser som tillhör en bilduppsättning.

Sidåterställning innebär att [!DNL eCatalog] bör starta en ny sida. `RenderSet` anger att det är en del av en `RenderSet` färgruta. Värdet måste `true` for `eCatalog` och `RenderSet` uppsättningar.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| resurs | `type:Asset` | Resurser i bilduppsättningsarrayen. |
| pageReset | `xsd:boolean` | Startar en ny sida. Inställningen ignoreras och värdet tvingas `true` for `eCatalog` och `RenderSet` uppsättningar. |
