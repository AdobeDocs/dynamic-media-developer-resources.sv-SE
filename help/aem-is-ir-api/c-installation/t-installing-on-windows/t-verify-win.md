---
title: Verifierar installationen
description: När du har installerat Dynamic Media Image Serving bör du verifiera installationen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Verifierar installationen {#verifying-the-installation}

När du har installerat Dynamic Media Image Serving bör du verifiera installationen.

Bildservern är installerad som en Windows-tjänst.

1. Öppna kontrollpanelen för tjänster och kontrollera att `Dynamic Media Image Serving` har statusen `Started`.
1. Öppna en webbläsare på samma eller en annan värd och kontrollera serverns standardsvar:

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

Kontrollera om det finns `imageServer.`-objekt i svaret, vilket anger att Image Server lyssnar.
>Ytterligare verifiering kan utföras med exempelsidorna i dokumentations- och demopaketen, om det är installerat.
