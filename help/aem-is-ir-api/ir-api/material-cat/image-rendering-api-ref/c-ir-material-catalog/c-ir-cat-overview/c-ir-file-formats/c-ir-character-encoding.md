---
description: Bildåtergivning stöder materialkataloger med ISO-8859-1 och UTF-8-kodning.
solution: Experience Manager
title: Teckenkodning
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Teckenkodning{#character-encoding}

Bildåtergivning stöder materialkataloger med ISO-8859-1 och UTF-8-kodning.

Ett byteordningsmärke (BOM) används för att ange kodningen för varje fil. För UTF-8 är byteordningen `EF BB BF`. UTF-8-kodning antas när den här teckensekvensen identifieras i början av varje materialkatalogfil. Andra bytesekvenser resulterar i att filen tolkas som kodad enligt standarden ISO-8859-1.

I många samtidiga program infogas BOM automatiskt när de är konfigurerade för UTF-8.
