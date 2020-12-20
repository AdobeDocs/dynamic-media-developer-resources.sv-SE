---
description: När du har installerat Scene7 Image Serving bör du verifiera installationen.
seo-description: När du har installerat Scene7 Image Serving bör du verifiera installationen.
seo-title: Verifierar installationen
solution: Experience Manager
title: Verifierar installationen
topic: Scene7 Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# Verifierar installationen{#verifying-the-installation}

När du har installerat Scene7 Image Serving bör du verifiera installationen.

Bildservern är installerad som en Windows-tjänst.

1. Öppna kontrollpanelen Tjänster och kontrollera att &quot;Scene7 Image Serving&quot; har statusen &quot;Started&quot;.
1. Öppna en webbläsare på samma eller en annan värd och kontrollera serverns standardsvar:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Kontrollera om det finns `imageServer.`-objekt i svaret, vilket anger att Image Server lyssnar.
>Ytterligare verifiering kan utföras med exempelsidorna i dokumentations- och demopaketen, om det är installerat.

