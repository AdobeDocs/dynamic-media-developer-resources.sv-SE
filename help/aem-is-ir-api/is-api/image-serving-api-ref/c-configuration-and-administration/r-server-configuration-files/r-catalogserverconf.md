---
description: Innehåller inställningar för hantering av bildkataloger.
seo-description: Innehåller inställningar för hantering av bildkataloger.
seo-title: catalog-server.conf
solution: Experience Manager
title: catalog-server.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 797a43d2-18f5-4735-8b19-da231952b1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
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
