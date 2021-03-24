---
description: Innehåller inställningar för hantering av bildkataloger.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# catalog-server.conf{#catalog-server-conf}

Innehåller inställningar för hantering av bildkataloger.

Filen är en JAVA-egenskapsfil. Det är viktigt att följa tillämpliga konventioner. annars kan det hända att plattformsservern inte kan startas. Använd ett dubbelt omvänt snedstreck (\\) eller ett enkelt snedstreck (/) i stället för ett omvänt snedstreck (\) i Windows-filsökvägar. Det omvända snedstrecket används som ett escape-tecken i den här filtypen.

Ändringarna i den här filen börjar gälla kort efter att filen har sparats.

Endast inställningarna nedan kan ändras i [!DNL catalog-service.conf]. Om en viss inställning saknas kan den läggas till var som helst i filen. Endast en instans av varje inställning kan finnas.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
