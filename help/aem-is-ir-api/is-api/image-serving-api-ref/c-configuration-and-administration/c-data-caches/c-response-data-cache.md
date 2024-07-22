---
title: Cache för svarsdata
description: ' [!DNL Platform Server]  cachelagrar alla svarsbilder och vissa textdata till disken om inte en begäran har markerats som otillgänglig.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Cache för svarsdata{#response-data-cache}

[!DNL Platform Server] cachelagrar alla svarsbilder och vissa textdata till disken om inte en begäran har markerats som icke-cachelagrad.

Platsen för diskcachen för [!DNL Platform Server] anges med `PS::cache.rootPaths`.

För program som har höga träfffrekvenser i cacheminnet kan du öka serverns prestanda och kapacitet genom att distribuera svarsdatacachen mellan flera diskenheter. Du uppnår detta genom att skapa en cacherotmapp på varje disk och registrera dem i `PS::cache.rootPaths`.

`PS::cache.maxSize` anger den totala storleken för alla cacheposter, utan hänsyn till någon belastning i filsystemet. Hur mycket diskutrymme som krävs beror på filsystemets egenskaper, t.ex. diskblockets storlek och antalet cacheposter. Reservera dubbelt så mycket diskutrymme för HTTP-diskcache som den mängd som anges av `PS::cache.maxSize`. En algoritm som används senast används för att hålla mängden cachelagrade data inom gränsen.

Förutom `PS::cache.maxSize` hanteras även svarscachen genom att det maximala antalet cacheposter begränsas med `PS::cache.maxEntries`. I Linux® måste den här inställningen ange ett värde som inte är större än antalet tillgängliga noder i cachepartitionen.

>[!NOTE]
>
>[!DNL Platform Server] underhåller ett cacheindex i minnet. Indexets storlek är 32 byte gånger värdet `PS::cache.maxEntries`. Öka stackstorleken för [!DNL Platform Server] så att större cacheminnen får plats, om det behövs.

Systemet använder en cacheindexfil som sparas på disken när servern stängs av på ett ordnat sätt. Om det inträffar oväntade händelser, t.ex. ett strömavbrott, kanske filen inte sparas. Det kan också ta flera minuter innan [!DNL Platform Server] blir klar.
