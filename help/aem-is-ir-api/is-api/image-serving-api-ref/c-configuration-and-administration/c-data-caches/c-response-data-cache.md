---
description: Plattformsservern cachelagrar alla svarsbilder och vissa textdata till disken, såvida inte en begäran har markerats som icke-cachelagrad.
solution: Experience Manager
title: Cache för svarsdata
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '302'
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
>Plattformsservern underhåller ett cacheindex i minnet. Indexets storlek är 32 byte gånger värdet `PS::cache.maxEntries`. Du kan behöva öka stackstorleken för Platform Server för att kunna hantera större cacheminnen.

Systemet använder en cacheindexfil som sparas på disken när servern stängs av på ett ordnat sätt. Om det inträffar oväntade händelser, t.ex. ett strömavbrott, kanske filen inte sparas. Det kan dessutom ta flera minuter för plattformsservern att bli klar.
