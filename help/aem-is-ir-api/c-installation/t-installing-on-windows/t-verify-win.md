---
description: När du har installerat Dynamic Media Image Serving bör du verifiera installationen.
seo-description: När du har installerat Dynamic Media Image Serving bör du verifiera installationen.
seo-title: Verifierar installationen
solution: Experience Manager
title: Verifierar installationen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Verifierar installationen{#verifying-the-installation}

När du har installerat Dynamic Media Image Serving bör du verifiera installationen.

Bildservern är installerad som en Windows-tjänst.

1. Öppna kontrollpanelen Tjänster och kontrollera att &quot;Dynamic Media Image Serving&quot; har statusen &quot;Started&quot;.
1. Öppna en webbläsare på samma eller en annan värd och kontrollera serverns standardsvar:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Kontrollera om det finns `imageServer.`-objekt i svaret, vilket anger att Image Server lyssnar.
>Ytterligare verifiering kan utföras med exempelsidorna i dokumentations- och demopaketen, om det är installerat.

