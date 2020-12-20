---
description: Kontrollera installationen när du har installerat Image Serving i Linux.
seo-description: Kontrollera installationen när du har installerat Image Serving i Linux.
seo-title: Verifierar installationen
solution: Experience Manager
title: Verifierar installationen
topic: Scene7 Image Serving - Image Rendering API
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---


# Verifierar installationen{#verifying-the-installation}

Kontrollera installationen när du har installerat Image Serving i Linux.

Image Server är installerad som Linux-daemon.

**Verifiera installationen**

1. Kontrollera att Image Serving är konfigurerad att starta automatiskt och att den körs:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Du måste ha rotbehörighet för att köra dessa skript.

1. Öppna en webbläsare på samma eller en annan värd och kontrollera serverns standardsvar:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

I svaren kontrollerar du om det finns objekt som börjar med &quot; `imageServer.`&quot;, vilket anger att plattformsservern kunde kommunicera med Image Server.
>Ytterligare verifiering kan utföras med exempelsidorna i dokumentations- och demopaketen, om det är installerat.

