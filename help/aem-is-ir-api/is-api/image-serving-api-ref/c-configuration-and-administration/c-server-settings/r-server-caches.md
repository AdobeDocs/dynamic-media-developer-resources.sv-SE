---
description: Använd de här serverinställningarna för servercachen.
seo-description: Använd de här serverinställningarna för servercachen.
seo-title: Servercacheminnen
solution: Experience Manager
title: Servercacheminnen
topic: Scene7 Image Serving - Image Rendering API
uuid: 73745363-2011-453f-b7a0-96de4b44186d
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# Servercacheminnen{#server-caches}

Använd de här serverinställningarna för servercachen.

## PS::cache.rootPaths - Cachelagra datamappar {#section-f0aa808304d74ecdb0c3644f11906c53}

Rotmappen för plattformsserverns diskcache. En eller flera absoluta filsökvägar eller sökvägar i förhållande till *[!DNL install_folder]*, avgränsade med semikolon (;). Data för HTTP-svarscachen kommer att fördelas jämnt över alla angivna mappar. Cacheminnen för hjälpcacheminnen (kompilerade bildkataloger och externa bilddata) finns i den primära cachemappen (den första mappen i listan).

## PS::cache.maxSize - Cachestorlek för svarsdata {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

Maximal storlek för HTTP-svarscache i byte. Denna inställning begränsar mängden faktiska data som ska cachas. det tar inte hänsyn till filsystemets belastning. (Se [Svarsdatacache](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Om flera cachedatamappar anges kommer cachedata att fördelas jämnt över alla mappar. Värdet `cache.maxSize` i [!DNL PlatformServer.conf] är i byte.

## PS::cache.maxEnentries - Max antal poster för svarsdatacache {#section-5603e327e90542a5b50aeeb27b080410}

Antalet poster som allokerats för indexet för HTTP-svarscache i minnet.

>[!NOTE]
>
>I Linux måste du se till att det finns tillräckligt med i-noder för cachepartitionen för att undvika att i-noderna tar slut.

## IS::TempDirectory - mappen temporära filer för bildservern {#section-42ea1e7a68c444878f7245c5bbcb1672}

Image Server behöver ibland spara mellanliggande data på disken. Sökvägen kan vara absolut eller relativ till *[!DNL install_folder]*.

>[!NOTE]
>
>Den nya mappen måste skapas innan den här inställningen ändras. Kontrollera att åtkomstbehörigheterna är inställda så att Image Server har fullständig kontroll över mappen.

## SV::temp - Mappen Temporära filer för serveransvarig {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Serverhanteraren behöver ibland spara mellanliggande data på disken. Sökvägen kan vara absolut eller relativ till *[!DNL install_folder]*. Standardvärdet är [!DNL *[!DNL install_folder]*/temp].

>[!NOTE]
>
>Den nya mappen måste skapas innan den här inställningen ändras. Se till att åtkomstbehörigheterna är inställda så att Server Supervisor har fullständig kontroll över mappen.

