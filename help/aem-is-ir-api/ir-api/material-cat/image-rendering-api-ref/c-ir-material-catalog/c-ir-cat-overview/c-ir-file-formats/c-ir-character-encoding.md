---
description: Bildåtergivning stöder materialkataloger med ISO-8859-1 och UTF-8-kodning.
solution: Experience Manager
title: Teckenkodning
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Teckenkodning{#character-encoding}

Bildåtergivning stöder materialkataloger med ISO-8859-1 och UTF-8-kodning.

Ett byteordningsmärke (BOM) används för att ange kodningen för varje fil. För UTF-8 är byteordningen `EF BB BF`. UTF-8-kodning antas när den här teckensekvensen identifieras i början av varje materialkatalogfil. Andra bytesekvenser resulterar i att filen tolkas som kodad enligt standarden ISO-8859-1.

I många samtidiga program infogas BOM automatiskt när de är konfigurerade för UTF-8.
