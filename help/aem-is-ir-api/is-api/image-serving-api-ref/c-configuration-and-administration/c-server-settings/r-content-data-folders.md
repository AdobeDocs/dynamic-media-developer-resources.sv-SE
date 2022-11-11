---
description: Använd de här serverinställningarna för innehållets datamappar.
solution: Experience Manager
title: Innehållsdatamappar
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Innehållsdatamappar{#content-data-folders}

Använd de här serverinställningarna för innehållets datamappar.

## IS::RootPath - rotmappar för bilddata {#section-5c57569514bb4d00b19de31d2e137e3b}

Platsen för alla källdata, inklusive bilder, teckensnitt och ICC-profiler. Detta kan vara en eller flera absoluta filsökvägar eller sökvägar i förhållande till *[!DNL install_folder]*, avgränsade med semikolon. Om tom *[!DNL install_folder]* är standardroten. Flera värden kan anges för att distribuera bilddata i flera filsystem. Image Server kommer att försöka med rotsökvägarna i den ordning som anges tills den begärda filen hittas.

## PS::staticContent.rootPath - rotmappar för statiska innehållsdata {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

Platsen för statiska innehållskälldata som ska levereras via [!DNL /is/static] kontext. Kan vara en eller flera absoluta filsökvägar eller sökvägar i förhållande till *[!DNL install_folder]*, avgränsade med semikolon. Om tom *[!DNL install_folder]* är standardroten.

Flera värden kan anges avgränsade med semikolon för att distribuera statiskt innehåll i flera filsystem. Vanligtvis inställd på samma värden som `IS::RootPath`.

The [!DNL Platform Server] testar rotsökvägarna i den ordning som anges tills den begärda filen hittas.

>[!NOTE]
>
>Som standard är det här fältet avsiktligt inställt på en icke-befintlig plats ( [!DNL *[!DNL install_folder]*/static]), inaktiverar den statiska innehållstjänsten.

## IS::SaveDirectory - mappen Spara rotfil {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Rotsökvägen för `attribute::SavePath` (används av `req=saveToFile`). Image Server måste ha behörighet att skapa åtkomstbehörigheter för den undermapp där bildfiler ska skapas.
