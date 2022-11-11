---
description: Använd de här serverinställningarna för SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# SSL{#ssl}

Använd de här serverinställningarna för SSL.

## TC::SslPort - avlyssningsport {#section-c80eb582bf684b3fa7313a77cc606769}

Anger avlyssningsporten för [!DNL Platform Server] för SSL-anslutningar. Standardvärdet är 8443.

## TC::keystoreFile - sökväg till nyckelbehållarfil {#section-0cdf9b3cfcf249818b22221d01bafebe}

Ange sökvägen/namnet för SSL-nyckelbehållarfilen. Kan vara en absolut sökväg eller en relativ sökväg till [!DNL] *[!DNL install_folder]*/conf]. Standard är *install_folder*/conf/scene7keystore.

## TC::keystorePass - lösenord för nyckelbehållare {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Lösenordet för nyckelfilen. Standard är `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Välj typ av nyckelbehållare. &#39; `Java'` (standard) och &#39; `PKCS12`&#39; stöds.
