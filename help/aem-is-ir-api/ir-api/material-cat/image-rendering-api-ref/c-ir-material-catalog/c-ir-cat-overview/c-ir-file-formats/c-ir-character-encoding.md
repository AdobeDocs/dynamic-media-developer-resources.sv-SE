---
description: Bildåtergivning stöder materialkataloger med ISO-8859-1 och UTF-8-kodning.
seo-description: Bildåtergivning stöder materialkataloger med ISO-8859-1 och UTF-8-kodning.
seo-title: Teckenkodning
solution: Experience Manager
title: Teckenkodning
topic: Dynamic Media Image Serving - Image Rendering API
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Teckenkodning{#character-encoding}

Bildåtergivning stöder materialkataloger med ISO-8859-1 och UTF-8-kodning.

Ett byteordningsmärke (BOM) används för att ange kodningen för varje fil. För UTF-8 är byteordningen `EF BB BF`. UTF-8-kodning antas när den här teckensekvensen identifieras i början av varje materialkatalogfil. Andra bytesekvenser resulterar i att filen tolkas som kodad enligt standarden ISO-8859-1.

I många samtidiga program infogas BOM automatiskt när de är konfigurerade för UTF-8.
