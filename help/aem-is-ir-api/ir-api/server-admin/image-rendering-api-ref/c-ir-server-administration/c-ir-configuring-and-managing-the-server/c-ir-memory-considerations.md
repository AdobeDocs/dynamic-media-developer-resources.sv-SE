---
description: Mängden minne som används för bildåtergivning kan variera mycket och beror i hög grad på den faktiska serverbelastningen och användningen (t.ex. några vinjetteringar, storlek och komplexitet för vinjetter osv.).
solution: Experience Manager
title: Minnesöverväganden
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# Minnesöverväganden{#memory-considerations}

Mängden minne som används för bildåtergivning kan variera mycket och beror i hög grad på den faktiska serverbelastningen och användningen (t.ex. några vinjetteringar, storlek och komplexitet för vinjetter osv.).

För bästa prestanda bör minnesväxling (växling) undvikas.

Bildåtergivning delar minneshanteringen för Image Server. När du använder bildåtergivning bör ytterligare minne allokeras. 30 till 50 % av det fysiska minnet kan vara rimligt.

Mer information om hur du ändrar minnesallokeringen för Image Server (ImageServer::PhysicalMemory) finns i dokumentationen för Image Serving.
