---
description: Image Serving stöder bildkataloger med ISO-8859-1 och UTF-8-kodning.
solution: Experience Manager
title: Teckenkodning
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Teckenkodning{#character-encoding}

Image Serving stöder bildkataloger med ISO-8859-1 och UTF-8-kodning.

Ett byteordningsmärke (BOM) används för att ange kodningen för varje fil. För UTF-8 är bytesekvensen BOM `EF BB BF`. UTF-8-kodning antas när den här teckensekvensen identifieras i början av varje bildkatalogfil. Andra bytesekvenser resulterar i att filen tolkas som kodad enligt standarden ISO-8859-1.

I många moderna program, som konfigurerats för UTF-8, infogas strukturlistan automatiskt.
