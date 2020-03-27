---
description: Använd de här serverinställningarna för SSL.
seo-description: Använd de här serverinställningarna för SSL.
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SSL{#ssl}

Använd de här serverinställningarna för SSL.

## TC::SslPort - avlyssningsport {#section-c80eb582bf684b3fa7313a77cc606769}

Anger avlyssningsporten för plattformsservern för SSL-anslutningar. Standardvärdet är 8443.

## TC::keystoreFile - sökväg till nyckelbehållarfil {#section-0cdf9b3cfcf249818b22221d01bafebe}

Ange sökvägen/namnet för SSL-nyckelbehållarfilen. Kan vara en absolut sökväg eller en relativ sökväg till [!DNL *[!DNL install_folder]*/conf]. Standard är *install_folder*/conf/scene7keystore.

## TC::keystorePass - lösenord för nyckelbehållare {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Lösenordet för nyckelfilen. Standardvärdet är `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Välj typ av nyckelbehållare. &#39; `Java'` (standard) och &#39; `PKCS12`&#39; stöds.
