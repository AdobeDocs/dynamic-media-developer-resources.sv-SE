---
description: Aktivera senaste ändrade svarshuvuden. Aktiverar eller inaktiverar inkludering av den senast ändrade rubriken i tillgängliga HTTP-svar som genereras av Image Serving.
seo-description: Aktivera senaste ändrade svarshuvuden. Aktiverar eller inaktiverar inkludering av den senast ändrade rubriken i tillgängliga HTTP-svar som genereras av Image Serving.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

Aktivera senaste ändrade svarshuvuden. Aktiverar eller inaktiverar inkludering av den senast ändrade rubriken i tillgängliga HTTP-svar som genereras av Image Serving.

Servern använder det senaste `catalog::TimeStamp` värdet för alla kataloger/katalogobjekt som ingår i ett svar som rubrikvärde Senaste ändring.

Bör bara aktiveras om ett distribuerat cachningsnätverk eller ett annat cachningssystem som inte stöder tagghuvuden används.

>[!NOTE]
>
>Försiktighet måste iakttas när du använder de senast ändrade rubrikerna i en belastningsutjämnad miljö som innefattar flera Image Serving-värdar. Klientcachning kan besegras och serverbelastningen ökar om servrarna av någon anledning har olika tidsstämplar för samma katalogposter. En sådan situation kan uppstå på följande sätt:
>
>* Varken `catalog::TimeStamp` eller `attribute::TimeStamp`så att ändringstiden för [!DNL catalog.ini] filen används som standard för `catalog::TimeStamp`.
   >
   >
* I stället för att dela bildkatalogfilerna via ett nätverk har varje server en egen instans av katalogfilerna på ett lokalt filsystem.
>* Två eller flera förekomster av samma [!DNL catalog.ini] fil har olika ändringsdatum, vilket kan bero på felaktig kopiering av filerna.
>



## Egenskaper {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Flagga. 0 för att inaktivera, 1 för att aktivera senast ändrade HTTP-huvuden.

## Standard {#section-4eb47aadab8b41609bef296a4115f9f4}

Ärvs från `default::UseLastModified` om inte definierad eller om tom.

## Se även {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[katalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
