---
description: Mängden minne som används för bildåtergivning kan variera mycket och beror i hög grad på den faktiska serverbelastningen och användningen (t.ex. några vinjetteringar, storlek och komplexitet för vinjetter osv.).
seo-description: Mängden minne som används för bildåtergivning kan variera mycket och beror i hög grad på den faktiska serverbelastningen och användningen (t.ex. några vinjetteringar, storlek och komplexitet för vinjetter osv.).
seo-title: Minnesöverväganden
solution: Experience Manager
title: Minnesöverväganden
topic: Scene7 Image Serving - Image Rendering API
uuid: 21247081-ff27-4237-93da-5fc996417dfd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# Minnesöverväganden{#memory-considerations}

Mängden minne som används för bildåtergivning kan variera mycket och beror i hög grad på den faktiska serverbelastningen och användningen (t.ex. några vinjetteringar, storlek och komplexitet för vinjetter osv.).

För bästa prestanda bör minnesväxling (växling) undvikas.

Bildåtergivning delar minneshanteringen för Image Server. När du använder bildåtergivning bör ytterligare minne allokeras. 30 till 50 % av det fysiska minnet kan vara rimligt.

Mer information om hur du ändrar minnesallokeringen för Image Server (ImageServer::PhysicalMemory) finns i dokumentationen för Image Serving.
