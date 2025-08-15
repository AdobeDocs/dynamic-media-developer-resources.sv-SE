---
description: Allmänna serverinställningar
solution: Experience Manager
title: Allmänt
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Allmänt{#general}

Allmänna serverinställningar

## TC::PsPort - huvudavlyssningsport {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Anger huvudavlyssningsporten för [!DNL Platform Server]. Den här porten används även för att komma åt dokumentation och exempelsidor för bildservrar, bildåtergivning och dynamiska medievyer (om de är installerade).

## IS::CacheServerUrl - URL för cachelagring av tjänstens rot {#section-bcca227a1f91453b834db4ea050968e2}

Anger HTTP-rotsökvägen som tillåter att Image Server får åtkomst till cachelagringstjänsten. Måste anges till [!DNL http://localhost:TC::PsPort /is/cache/secondary], med portnumret som matchar `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - standard-TTL för fjärr-Image Source {#section-e4c31228b459492cacd2f482d9575f71}

TTL för cachelagrade bilder som hämtats via HTTP från en fjärrkälla med hjälp av `src={…}`-konstruktionen. Används endast när fjärrservern inte har något förfallohuvud i HTTP-svaret. Heltalsvärde i sekunder.

## IS::RemoteUrlTimeout - fjärrtimeout för Image Source {#section-437646c479cc4bea81dae42100a3c50a}

Den tid som Image Server väntar på att en fjärrserver ska leverera den begärda bildfilen via HTTP innan ett fel returneras. Heltalsvärde i sekunder.

## PS::allowDefaultCatalogRequests - Aktivera/inaktivera standardkatalogbegäranden {#section-484e442a115a49b4ac269d1718b351e1}

Ange som false om du inte vill tillåta begäranden som inte innehåller något giltigt katalog-ID i sökvägen. Standardvärdet är `true`. När värdet är `false` returneras ett fel för begäranden utan katalog-ID.

>[!NOTE]
>
>`req=catalogprops` omfattas inte av den här inställningen.

## PS::saveToFile.saveTimeout - Tidsgräns för filsparande {#section-d22afd8ad86144b28684ed95a59db40e}

Standardvärde för timeout för `req=saveToFile` när `timeout=`inte har angetts. `msec`. Ett fel returneras om sparåtgärden inte slutförs inom den angivna tiden.
