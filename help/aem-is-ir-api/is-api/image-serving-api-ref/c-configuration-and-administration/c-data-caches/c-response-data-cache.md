---
title: Cache för svarsdata
description: The [!DNL Platform Server] sparar alla svarsbilder och vissa textdata i cacheminnet, såvida inte en begäran har markerats som icke-cachelagrad.
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

The [!DNL Platform Server] sparar alla svarsbilder och vissa textdata i cacheminnet, såvida inte en begäran har markerats som icke-cachelagrad.

Platsen för [!DNL Platform Server]Diskcachen är inställd med `PS::cache.rootPaths`.

För program som har höga träfffrekvenser i cacheminnet kan du öka serverns prestanda och kapacitet genom att distribuera svarsdatacachen mellan flera diskenheter. Du uppnår detta genom att skapa en cacherotmapp på varje disk och registrera dem i `PS::cache.rootPaths`.

The `PS::cache.maxSize` Anger den totala storleken för alla cacheposter, utan hänsyn till någon belastning i filsystemet. Hur mycket diskutrymme som krävs beror på filsystemets egenskaper, t.ex. diskblockets storlek och antalet cacheposter. Reservera dubbelt så mycket diskutrymme för HTTP-diskcachen som den mängd som anges av `PS::cache.maxSize`. En algoritm som används senast används för att hålla mängden cachelagrade data inom gränsen.

Förutom `PS::cache.maxSize`, hanteras svarscachen också genom att det maximala antalet cacheposter begränsas med `PS::cache.maxEntries`. I Linux® måste den här inställningen ange ett värde som inte är större än antalet tillgängliga noder i cachepartitionen.

>[!NOTE]
>
>The [!DNL Platform Server] underhåller ett cacheindex i minnet. Indexets storlek är 32 byte gånger värdet för `PS::cache.maxEntries`. Öka [!DNL Platform Server] stackstorlek för att rymma större cacheminnen, om det behövs.

Systemet använder en cacheindexfil som sparas på disken när servern stängs av på ett ordnat sätt. Om det inträffar oväntade händelser, t.ex. ett strömavbrott, kanske filen inte sparas. Dessutom kan det ta flera minuter för [!DNL Platform Server] för att bli redo.
