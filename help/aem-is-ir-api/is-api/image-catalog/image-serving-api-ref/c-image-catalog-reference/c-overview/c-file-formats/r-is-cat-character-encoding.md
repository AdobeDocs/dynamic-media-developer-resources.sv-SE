---
description: Image Serving stöder bildkataloger med ISO-8859-1 och UTF-8-kodning.
seo-description: Image Serving stöder bildkataloger med ISO-8859-1 och UTF-8-kodning.
seo-title: Teckenkodning
solution: Experience Manager
title: Teckenkodning
topic: Scene7 Image Serving - Image Rendering API
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Teckenkodning{#character-encoding}

Image Serving stöder bildkataloger med ISO-8859-1 och UTF-8-kodning.

Ett byteordningsmärke (BOM) används för att ange kodningen för varje fil. För UTF-8 är bytesekvensen BOM `EF BB BF`. UTF-8-kodning antas när den här teckensekvensen identifieras i början av varje bildkatalogfil. Andra bytesekvenser resulterar i att filen tolkas som kodad enligt standarden ISO-8859-1.

I många moderna program, som konfigurerats för UTF-8, infogas strukturlistan automatiskt.
