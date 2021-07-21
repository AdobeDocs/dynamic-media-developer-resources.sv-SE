---
description: Mängden minne som används för bildåtergivning kan variera mycket och beror i hög grad på den faktiska serverbelastningen och användningen (t.ex. några vinjetteringar, storlek och komplexitet för vinjetter osv.).
solution: Experience Manager
title: Minnesöverväganden
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Minnesöverväganden{#memory-considerations}

Mängden minne som används för bildåtergivning kan variera mycket och beror i hög grad på den faktiska serverbelastningen och användningen (t.ex. några vinjetteringar, storlek och komplexitet för vinjetter osv.).

För bästa prestanda bör minnesväxling (växling) undvikas.

Bildåtergivning delar minneshanteringen för Image Server. När du använder bildåtergivning bör ytterligare minne allokeras. 30 till 50 % av det fysiska minnet kan vara rimligt.

Mer information om hur du ändrar minnesallokeringen för Image Server (ImageServer::PhysicalMemory) finns i dokumentationen för Image Serving.
