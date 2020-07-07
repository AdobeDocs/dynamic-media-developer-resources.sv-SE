---
description: När det är enkelt och enkelt att lägga till nya datafiler måste du vara särskilt försiktig när du ersätter befintliga datafiler som aktivt används av servern. I stället för att bara ersätta sådana filer rekommenderar vi att du ger ersättningsfilen ett nytt namn (t.ex. lägger till ett versionssuffix till filnamnet). När den nya filen har publicerats kan den gamla versionen tas bort.
seo-description: När det är enkelt och enkelt att lägga till nya datafiler måste du vara särskilt försiktig när du ersätter befintliga datafiler som aktivt används av servern. I stället för att bara ersätta sådana filer rekommenderar vi att du ger ersättningsfilen ett nytt namn (t.ex. lägger till ett versionssuffix till filnamnet). När den nya filen har publicerats kan den gamla versionen tas bort.
seo-title: Ta bort eller ersätta datafiler
solution: Experience Manager
title: Ta bort eller ersätta datafiler
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b446144-48f6-4b50-93ec-0287425d932a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---


# Ta bort eller ersätta datafiler{#deleting-or-replacing-data-files}

När det är enkelt och enkelt att lägga till nya datafiler måste du vara särskilt försiktig när du ersätter befintliga datafiler som aktivt används av servern. I stället för att bara ersätta sådana filer rekommenderar vi att du ger ersättningsfilen ett nytt namn (t.ex. lägger till ett versionssuffix till filnamnet). När den nya filen har publicerats kan den gamla versionen tas bort.

>[!NOTE]
>
>Datafiler ska aldrig ersättas eller tas bort när de används aktivt av bildservern. Fel eller till och med en serverkrasch kan inträffa i annat fall.

Kom ihåg att cacheposterna för Platform Server och klientcachen måste bli inaktuella innan de uppdaterade data kan ses av klienten. Du kan uppdatera specifika cacheposter direkt med `cache=validate` kommandot.

Ändringar i teckensnittsfiler och ICC-profilfiler spåras inte direkt av cachehanteraren. Om en sådan resurs ändras utan att dess ID ändras, kommer servercachen inte att känna till ändringen och `cache=validate` kommer inte att göra att cacheposten uppdateras. `cache=update` kan användas för att framtvinga återskapande av sådana cacheposter.

Du bör ge en ersättningsfil ett nytt namn och uppdatera motsvarande katalogposter för att undvika komplikationer med att ersätta filer. Detta gör att du kan ersätta en datafil medan servern är aktiv och göra så att servercacheposter blir inaktuella omedelbart utan någon ytterligare åtgärd. Den här metoden kan användas för ICC-profiler, teckensnitt och alla bilder som hanteras av bildkataloger.
