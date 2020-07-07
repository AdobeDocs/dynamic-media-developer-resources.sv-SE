---
description: Vinjetteringsfiler kan ersättas eller tas bort medan servern är aktiv genom att använda kommandot req=release precis innan filen skrivs över.
seo-description: Vinjetteringsfiler kan ersättas eller tas bort medan servern är aktiv genom att använda kommandot req=release precis innan filen skrivs över.
seo-title: Ta bort eller ersätta källdatafiler
solution: Experience Manager
title: Ta bort eller ersätta källdatafiler
topic: Scene7 Image Serving - Image Rendering API
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Ta bort eller ersätta källdatafiler{#deleting-or-replacing-source-data-files}

Vinjetteringsfiler kan ersättas eller tas bort medan servern är aktiv genom att använda kommandot req=release precis innan filen skrivs över.

>[!NOTE]
>
>En datafil får inte ersättas eller tas bort medan återgivningsservern använder den.

Tänk på att om du tar bort eller ersätter en källdatafil kommer återgivningsservern bara att stänga filen tills nästa begäran som får åtkomst till den vinjetteringen. Flera försök kan behövas om en fil används i stor utsträckning.

Återgivningsservern måste stoppas för att andra datafiler ska kunna ersättas.

Cacheposter för Platform Server ogiltigförklaras automatiskt när materialfiler eller vinjetter ersätts. Att ersätta ICC-profilfiler gör inte cacheminnen ogiltiga.

Du bör ge en ersättningsfil ett nytt namn och uppdatera motsvarande katalogposter för att undvika komplikationer med att ersätta filer. Detta gör att du kan ersätta en datafil medan servern är aktiv och gör att servercacheposter blir inaktuella automatiskt utan ytterligare åtgärder. Den här metoden kan användas för alla datafiler som hanteras av bildkataloger.
