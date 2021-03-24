---
description: Resurser som tillhör en bilduppsättning.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Bilduppsättningar
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---


# ImageSetMember{#imagesetmember}

Resurser som tillhör en bilduppsättning.

Sidåterställning innebär att en [!DNL eCatalog] ska starta en ny sida. `RenderSet` visar att det är en del av en  `RenderSet` färgruta. Värdet tvingas till `true` för `eCatalog`- och `RenderSet`-uppsättningar.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`resurs`*` | `type:Asset` | Resurser i bilduppsättningsarrayen. |
| `*`pageReset`*` | `xsd:boolean` | Startar en ny sida. Inställningen ignoreras och värdet tvingas till `true` för uppsättningarna `eCatalog` och `RenderSet`. |

