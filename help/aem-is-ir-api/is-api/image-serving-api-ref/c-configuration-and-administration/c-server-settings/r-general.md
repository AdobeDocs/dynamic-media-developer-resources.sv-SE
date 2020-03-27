---
description: Allmänna serverinställningar
seo-description: Allmänna serverinställningar
seo-title: Allmänt
solution: Experience Manager
title: Allmänt
topic: Scene7 Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Allmänt{#general}

Allmänna serverinställningar

## TC::PsPort - huvudavlyssningsport {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Anger den huvudsakliga avlyssningsporten för plattformsservern. Den här porten används också för att komma åt dokumentation och exempelsidor för bildservrar, bildåtergivning och Scene7-visningsprogram (om de är installerade).

## IS::CacheServerUrl - URL för cachelagring av tjänstens rot {#section-bcca227a1f91453b834db4ea050968e2}

Anger HTTP-rotsökvägen som tillåter att Image Server får åtkomst till cachelagringstjänsten. Måste anges till [!DNL http://localhost:TC::PsPort /is/cache/secondary], med matchande portnummer `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - Fjärrbildskällans standard-TTL {#section-e4c31228b459492cacd2f482d9575f71}

TTL för cachelagrade bilder som hämtas via HTTP från en fjärrkälla med hjälp av `src={…}` konstruktionen. Används endast när fjärrservern inte har något förfallohuvud i HTTP-svaret. Heltalsvärde i sekunder.

## IS::RemoteUrlTimeout - timeout för fjärrbildskälla {#section-437646c479cc4bea81dae42100a3c50a}

Den tid som Image Server väntar på att en fjärrserver ska leverera den begärda bildfilen via HTTP innan ett fel returneras. Heltalsvärde i sekunder.

## PS::allowDefaultCatalogRequests - Aktivera/inaktivera standardkatalogbegäranden {#section-484e442a115a49b4ac269d1718b351e1}

Ange som false om du inte vill tillåta begäranden som inte innehåller något giltigt katalog-ID i sökvägen. Standardvärdet är `true`. När den anges `false`returneras ett fel för begäranden utan katalog-ID.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>`req=catalogprops` omfattas inte av den här inställningen.

## PS::saveToFile.saveTimeout - Tidsgräns för filsparande {#section-d22afd8ad86144b28684ed95a59db40e}

Standardvärde för timeout för `req=saveToFile` när `timeout=`inte anges. `msec`. Ett fel returneras om sparandet inte slutförs inom den angivna tiden.
