---
description: Resurser som tillhör en bilduppsättning.
seo-description: Resurser som tillhör en bilduppsättning.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
topic: Scene7 Image Production System API
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---


# ImageSetMember{#imagesetmember}

Resurser som tillhör en bilduppsättning.

Sidåterställning innebär att en [!DNL eCatalog] ska starta en ny sida. `RenderSet` visar att det är en del av en  `RenderSet` färgruta. Värdet tvingas till `true` för `eCatalog`- och `RenderSet`-uppsättningar.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| ` *`resurs`*` | `type:Asset` | Resurser i bilduppsättningsarrayen. |
| ` *`pageReset`*` | `xsd:boolean` | Startar en ny sida. Inställningen ignoreras och värdet tvingas till `true` för uppsättningarna `eCatalog` och `RenderSet`. |

