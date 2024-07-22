---
description: Vinjetteringsfiler kan ersättas eller tas bort medan servern är aktiv genom att använda kommandot req=release precis innan filen skrivs över.
solution: Experience Manager
title: Ta bort eller ersätta källdatafiler
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Ta bort eller ersätta källdatafiler{#deleting-or-replacing-source-data-files}

Vinjetteringsfiler kan ersättas eller tas bort medan servern är aktiv genom att använda kommandot req=release precis innan filen skrivs över.

>[!NOTE]
>
>En datafil får inte ersättas eller tas bort medan återgivningsservern använder den.

Tänk på att om du tar bort eller ersätter en källdatafil kommer återgivningsservern bara att stänga filen tills nästa begäran som får åtkomst till den vinjetteringen. Flera försök kan behövas om en fil används i stor utsträckning.

Återgivningsservern måste stoppas för att andra datafiler ska kunna ersättas.

[!DNL Platform Server] cacheposter ogiltigförklaras automatiskt när materialfiler eller vinjetter ersätts. Att ersätta ICC-profilfiler gör inte cacheminnen ogiltiga.

Du bör ge en ersättningsfil ett nytt namn och uppdatera motsvarande katalogposter för att undvika komplikationer med att ersätta filer. Detta gör att du kan ersätta en datafil medan servern är aktiv och gör att servercacheposter blir inaktuella automatiskt utan ytterligare åtgärder. Den här metoden kan användas för alla datafiler som hanteras av bildkataloger.
