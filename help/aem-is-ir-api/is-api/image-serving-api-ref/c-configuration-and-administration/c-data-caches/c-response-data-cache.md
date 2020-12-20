---
description: Plattformsservern cachelagrar alla svarsbilder och vissa textdata till disken, såvida inte en begäran har markerats som icke-cachelagrad.
seo-description: Plattformsservern cachelagrar alla svarsbilder och vissa textdata till disken, såvida inte en begäran har markerats som icke-cachelagrad.
seo-title: Cache för svarsdata
solution: Experience Manager
title: Cache för svarsdata
topic: Scene7 Image Serving - Image Rendering API
uuid: dbfda210-3b50-4e8c-8d77-7263ae4e80a2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Svarsdatacache{#response-data-cache}

Plattformsservern cachelagrar alla svarsbilder och vissa textdata till disken, såvida inte en begäran har markerats som icke-cachelagrad.

Platsen för plattformsserverns diskcache anges med `PS::cache.rootPaths`.

För program som har höga träfffrekvenser i cacheminnet kan du öka serverns prestanda och kapacitet genom att distribuera svarsdatacachen mellan flera diskenheter. Du uppnår detta genom att skapa en cacherotmapp på varje disk och registrera dem i `PS::cache.rootPaths`.

`PS::cache.maxSize` Anger den totala storleken för alla cacheposter, utan hänsyn till någon belastning i filsystemet. Hur mycket diskutrymme som krävs beror på filsystemets egenskaper, t.ex. diskblockets storlek och antalet cacheposter. Vi rekommenderar att du reserverar dubbelt så mycket diskutrymme för HTTP-diskcachen som den mängd som anges av `PS::cache.maxSize`. En algoritm som används senast används för att hålla mängden cachelagrade data inom gränsen.

Förutom `PS::cache.maxSize` hanteras även svarscachen genom att det maximala antalet cacheposter med `PS::cache.maxEntries` begränsas. I Linux måste den här inställningen ange ett värde som inte är större än antalet tillgängliga noder i cachepartitionen.

>[!NOTE]
>
>Plattformsservern underhåller ett cacheindex i minnet. Indexets storlek är 32 byte gånger värdet `PS::cache.maxEntries`. Du kan behöva öka stackstorleken för Platform Server för att få plats med större cacheminnen.

Systemet använder en cacheindexfil som sparas på disken när servern stängs av på ett ordnat sätt. Om det inträffar oväntade händelser, t.ex. ett strömavbrott, kanske filen inte sparas. Det kan dessutom ta flera minuter för plattformsservern att bli klar.
