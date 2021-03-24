---
description: När du har installerat Dynamic Media Image Serving bör du verifiera installationen.
solution: Experience Manager
title: Verifierar installationen
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '121'
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

