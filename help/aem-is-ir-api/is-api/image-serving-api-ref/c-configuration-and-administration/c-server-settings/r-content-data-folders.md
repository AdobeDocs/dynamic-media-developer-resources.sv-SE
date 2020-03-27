---
description: Använd de här serverinställningarna för innehållets datamappar.
seo-description: Använd de här serverinställningarna för innehållets datamappar.
seo-title: Innehållsdatamappar
solution: Experience Manager
title: Innehållsdatamappar
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Innehållsdatamappar{#content-data-folders}

Använd de här serverinställningarna för innehållets datamappar.

## IS::RootPath - rotmappar för bilddata {#section-5c57569514bb4d00b19de31d2e137e3b}

Platsen för alla källdata, inklusive bilder, teckensnitt och ICC-profiler. Detta kan vara en eller flera absoluta sökvägar eller sökvägar i förhållande till *[!DNL install_folder]*, avgränsade med semikolon. Om den är tom *[!DNL install_folder]* är standardroten. Flera värden kan anges för att distribuera bilddata i flera filsystem. Image Server kommer att försöka med rotsökvägarna i den ordning som anges tills den begärda filen hittas.

## PS::staticContent.rootPath - rotmappar för statiska innehållsdata {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

Platsen för statiska innehållskälldata som är avsedda att levereras via [!DNL /is/static] kontexten. Kan vara en eller flera absoluta filsökvägar eller sökvägar i förhållande till *[!DNL install_folder]*, avgränsade med semikolon. Om den är tom *[!DNL install_folder]* är standardroten.

Flera värden kan anges avgränsade med semikolon för att distribuera statiskt innehåll i flera filsystem. Vanligtvis inställd på samma värden som `IS::RootPath`.

Plattformsservern testar rotsökvägarna i den ordning som anges tills den begärda filen hittas.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Som standard är det här fältet avsiktligt inställt på en icke-befintlig plats ( [!DNL *[!DNL install_folder]*/static]), vilket inaktiverar den statiska innehållstjänsten.

## IS::SaveDirectory - mappen Spara rotfil {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Rotsökvägen för `attribute::SavePath` (används av `req=saveToFile`). Image Server måste ha behörighet att skapa åtkomstbehörigheter för den undermapp där bildfiler ska skapas.
