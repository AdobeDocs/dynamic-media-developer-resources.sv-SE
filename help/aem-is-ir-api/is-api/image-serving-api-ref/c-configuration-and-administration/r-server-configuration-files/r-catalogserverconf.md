---
description: Innehåller inställningar för hantering av bildkataloger.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

Innehåller inställningar för hantering av bildkataloger.

Filen är en JAVA-egenskapsfil. Du måste iaktta försiktighet för att följa lämpliga konventioner. Annars kanske [!DNL Platform Server] inte kan startas. Använd ett dubbelt omvänt snedstreck (\\) eller ett enkelt snedstreck (/) i stället för ett omvänt snedstreck (\) i Windows-filsökvägar. Det omvända snedstrecket används som ett escape-tecken i den här filtypen.

Ändringarna i den här filen börjar gälla kort efter att filen har sparats.

Endast inställningarna nedan kan ändras i [!DNL catalog-service.conf]. Om en viss inställning saknas kan den läggas till var som helst i filen. Endast en instans av varje inställning kan finnas.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
