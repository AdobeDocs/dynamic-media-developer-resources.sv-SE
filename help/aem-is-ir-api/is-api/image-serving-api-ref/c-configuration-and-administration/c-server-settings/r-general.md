---
description: Allmänna serverinställningar
seo-description: Allmänna serverinställningar
seo-title: Allmänt
solution: Experience Manager
title: Allmänt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Allmänt{#general}

Allmänna serverinställningar

## TC::PsPort - huvudavlyssningsport {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Anger den huvudsakliga avlyssningsporten för plattformsservern. Den här porten används även för att komma åt dokumentation och exempelsidor för Image Serving, Image Rendering och Dynamic Media Viewer (om det är installerat).

## IS::CacheServerUrl - Caching Service Root Url {#section-bcca227a1f91453b834db4ea050968e2}

Anger HTTP-rotsökvägen som tillåter att Image Server får åtkomst till cachelagringstjänsten. Måste anges till [!DNL http://localhost:TC::PsPort /is/cache/secondary], med portnumret som matchar `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - Fjärrbildskällans standard-TTL {#section-e4c31228b459492cacd2f482d9575f71}

TTL för cachelagrade bilder som hämtas via HTTP från en fjärrkälla med hjälp av `src={…}`-konstruktionen. Används endast när fjärrservern inte har något förfallohuvud i HTTP-svaret. Heltalsvärde i sekunder.

## IS::RemoteUrlTimeout - Timeout för fjärrbildskälla {#section-437646c479cc4bea81dae42100a3c50a}

Den tid som Image Server väntar på att en fjärrserver ska leverera den begärda bildfilen via HTTP innan ett fel returneras. Heltalsvärde i sekunder.

## PS::allowDefaultCatalogRequests - Aktivera/inaktivera standardkatalogbegäranden {#section-484e442a115a49b4ac269d1718b351e1}

Ange som false om du inte vill tillåta begäranden som inte innehåller något giltigt katalog-ID i sökvägen. Standardvärdet är `true`. Om `false` anges returneras ett fel för begäranden utan katalog-ID.

>[!NOTE]
>
>`req=catalogprops` omfattas inte av den här inställningen.

## PS::saveToFile.saveTimeout - Tidsgräns för filsparande {#section-d22afd8ad86144b28684ed95a59db40e}

Standardvärde för timeout för `req=saveToFile` när `timeout=`inte har angetts. `msec`. Ett fel returneras om sparandet inte slutförs inom den angivna tiden.
