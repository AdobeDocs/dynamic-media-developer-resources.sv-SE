---
description: Använd de här serverinställningarna för SSL.
seo-description: Använd de här serverinställningarna för SSL.
seo-title: SSL
solution: Experience Manager
title: SSL
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# SSL{#ssl}

Använd de här serverinställningarna för SSL.

## TC::SslPort - avlyssningsport {#section-c80eb582bf684b3fa7313a77cc606769}

Anger avlyssningsporten för plattformsservern för SSL-anslutningar. Standardvärdet är 8443.

## TC::keystoreFile - sökväg till nyckelfil {#section-0cdf9b3cfcf249818b22221d01bafebe}

Ange sökvägen/namnet för SSL-nyckelbehållarfilen. Kan vara en absolut sökväg eller en relativ sökväg till [!DNL *[!DNL install_folder]*/conf]. Standardvärdet är *install_folder*/conf/scene7keystore.

## TC::keystorePass - lösenord för nyckelbehållare {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Lösenordet för nyckelfilen. Standardvärdet är `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Välj typ av nyckelbehållare. &#39; `Java'` (standard) och &#39; `PKCS12`&#39; stöds.
