---
title: Verifierar installationen
description: Kontrollera installationen när du har installerat Image Serving i Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Verifierar installationen{#verifying-the-installation}

Kontrollera installationen när du har installerat Image Serving i Linux®.

Image Server är installerad som Linux® daemon.

**Verifiera installationen**

1. Kontrollera att Image Serving är konfigurerad att starta automatiskt och att den körs:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Du måste ha rotbehörighet för att köra dessa skript.

1. Öppna en webbläsare på samma eller en annan värd och kontrollera serverns standardsvar:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

I svaren kontrollerar du om det finns objekt som börjar med `imageServer`, vilket anger att [!DNL Platform Server] kan kommunicera med Image Server.

>Ytterligare verifiering kan utföras med exempelsidorna i dokumentations- och demopaketen, om det är installerat.
