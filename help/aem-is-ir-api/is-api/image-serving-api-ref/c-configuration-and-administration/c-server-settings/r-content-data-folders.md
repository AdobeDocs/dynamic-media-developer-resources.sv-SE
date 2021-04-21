---
description: Använd de här serverinställningarna för innehållets datamappar.
solution: Experience Manager
title: Innehållsdatamappar
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---


# Innehållsdatamappar{#content-data-folders}

Använd de här serverinställningarna för innehållets datamappar.

## IS::RootPath - Image Data Root Folders {#section-5c57569514bb4d00b19de31d2e137e3b}

Platsen för alla källdata, inklusive bilder, teckensnitt och ICC-profiler. Det kan vara en eller flera absoluta filsökvägar eller sökvägar i förhållande till *[!DNL install_folder]*, avgränsade med semikolon. Om den är tom är *[!DNL install_folder]* standardroten. Flera värden kan anges för att distribuera bilddata i flera filsystem. Image Server kommer att försöka med rotsökvägarna i den ordning som anges tills den begärda filen hittas.

## PS::staticContent.rootPath - rotmappar för statiska innehållsdata {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

Platsen för statiska innehållskälldata som ska levereras via [!DNL /is/static]-kontexten. Kan vara en eller flera absoluta filsökvägar eller sökvägar i förhållande till *[!DNL install_folder]*, avgränsade med semikolon. Om den är tom är *[!DNL install_folder]* standardroten.

Flera värden kan anges avgränsade med semikolon för att distribuera statiskt innehåll i flera filsystem. Använd vanligtvis samma värden som `IS::RootPath`.

Plattformsservern testar rotsökvägarna i den ordning som anges tills den begärda filen hittas.

>[!NOTE]
>
>Som standard är det här fältet avsiktligt inställt på en icke-befintlig plats ( [!DNL *[!DNL install_folder]*/static]), vilket inaktiverar den statiska innehållstjänsten.

## IS::SaveDirectory - filsparningsrotmapp {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Rotsökvägen för `attribute::SavePath` (används av `req=saveToFile`). Image Server måste ha behörighet att skapa åtkomstbehörigheter för den undermapp där bildfiler ska skapas.
