---
description: När det är enkelt och enkelt att lägga till nya datafiler måste du vara särskilt försiktig när du ersätter befintliga datafiler som aktivt används av servern. I stället för att bara ersätta sådana filer rekommenderar vi att du ger ersättningsfilen ett nytt namn (till exempel lägger till ett versionssuffix till filnamnet). När den nya filen har publicerats kan den gamla versionen tas bort.
solution: Experience Manager
title: Ta bort eller ersätta datafiler
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Ta bort eller ersätta datafiler{#deleting-or-replacing-data-files}

När det är enkelt och enkelt att lägga till nya datafiler måste du vara särskilt försiktig när du ersätter befintliga datafiler som aktivt används av servern. I stället för att bara ersätta sådana filer rekommenderar vi att du ger ersättningsfilen ett nytt namn (till exempel lägger till ett versionssuffix till filnamnet). När den nya filen har publicerats kan den gamla versionen tas bort.

>[!NOTE]
>
>Datafiler ska aldrig ersättas eller tas bort när de används aktivt av bildservern. Fel eller till och med en serverkrasch kan inträffa i annat fall.

Kom ihåg att cacheposterna [!DNL Platform Server] och klientens cacheposter måste bli inaktuella innan de uppdaterade data kan ses av klienten. Specifika cacheposter kan uppdateras omedelbart med kommandot `cache=validate`.

Ändringar i teckensnittsfiler och ICC-profilfiler spåras inte direkt av cachehanteraren. Om en sådan resurs ändras utan att dess ID ändras, känner inte servercachen till ändringen och `cache=validate` gör inte att cacheposten uppdateras. `cache=update` kan användas för att framtvinga återskapande av sådana cacheposter.

Du bör ge en ersättningsfil ett nytt namn och uppdatera motsvarande katalogposter för att undvika komplikationer med att ersätta filer. Detta gör att du kan ersätta en datafil medan servern är aktiv och få servercacheposter att bli inaktuella omedelbart utan ytterligare åtgärder. Den här metoden kan användas för ICC-profiler, teckensnitt och alla bilder som hanteras av bildkataloger.
