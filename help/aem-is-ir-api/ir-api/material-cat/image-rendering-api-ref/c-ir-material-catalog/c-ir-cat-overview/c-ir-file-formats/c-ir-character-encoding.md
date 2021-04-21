---
description: Bildåtergivning stöder materialkataloger med ISO-8859-1 och UTF-8-kodning.
solution: Experience Manager
title: Teckenkodning
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Teckenkodning{#character-encoding}

Bildåtergivning stöder materialkataloger med ISO-8859-1 och UTF-8-kodning.

Ett byteordningsmärke (BOM) används för att ange kodningen för varje fil. För UTF-8 är byteordningen `EF BB BF`. UTF-8-kodning antas när den här teckensekvensen identifieras i början av varje materialkatalogfil. Andra bytesekvenser resulterar i att filen tolkas som kodad enligt standarden ISO-8859-1.

I många samtidiga program infogas BOM automatiskt när de är konfigurerade för UTF-8.
