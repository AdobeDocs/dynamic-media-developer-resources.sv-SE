---
description: När det är enkelt och enkelt att lägga till nya datafiler måste du vara särskilt försiktig när du ersätter befintliga datafiler som aktivt används av servern. I stället för att bara ersätta sådana filer rekommenderar vi att du ger ersättningsfilen ett nytt namn (t.ex. lägger till ett versionssuffix till filnamnet). När den nya filen har publicerats kan den gamla versionen tas bort.
solution: Experience Manager
title: Ta bort eller ersätta datafiler
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Ta bort eller ersätta datafiler{#deleting-or-replacing-data-files}

När det är enkelt och enkelt att lägga till nya datafiler måste du vara särskilt försiktig när du ersätter befintliga datafiler som aktivt används av servern. I stället för att bara ersätta sådana filer rekommenderar vi att du ger ersättningsfilen ett nytt namn (t.ex. lägger till ett versionssuffix till filnamnet). När den nya filen har publicerats kan den gamla versionen tas bort.

>[!NOTE]
>
>Datafiler ska aldrig ersättas eller tas bort när de används aktivt av bildservern. Fel eller till och med en serverkrasch kan inträffa i annat fall.

Kom ihåg att [!DNL Platform Server] cache och klientens cacheposter måste bli inaktuella innan de uppdaterade data kan ses av klienten. Specifika cacheposter kan uppdateras omedelbart med `cache=validate` -kommando.

Ändringar i teckensnittsfiler och ICC-profilfiler spåras inte direkt av cachehanteraren. Om en sådan resurs ändras utan att dess ID ändras, kommer servercachen inte att känna till ändringen och `cache=validate` medför inte att cacheposten uppdateras. `cache=update` kan användas för att framtvinga återskapande av sådana cacheposter.

Du bör ge en ersättningsfil ett nytt namn och uppdatera motsvarande katalogposter för att undvika komplikationer med att ersätta filer. Detta gör att du kan ersätta en datafil medan servern är aktiv och göra så att servercacheposter blir inaktuella omedelbart utan någon ytterligare åtgärd. Den här metoden kan användas för ICC-profiler, teckensnitt och alla bilder som hanteras av bildkataloger.
