---
description: Aktivera senaste ändrade svarshuvuden. Aktiverar eller inaktiverar inkludering av den senast ändrade rubriken i tillgängliga HTTP-svar som genereras av Image Serving.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# UseLastModified{#uselastmodified}

Aktivera senaste ändrade svarshuvuden. Aktiverar eller inaktiverar inkludering av den senast ändrade rubriken i tillgängliga HTTP-svar som genereras av Image Serving.

Servern använder det senaste `catalog::TimeStamp`-värdet för alla kataloger/katalogposter som ingår i ett svar som det senast ändrade rubrikvärdet.

Bör bara aktiveras om ett distribuerat cachningsnätverk eller ett annat cachningssystem som inte stöder tagghuvuden används.

>[!NOTE]
>
>Försiktighet måste iakttas när du använder de senast ändrade rubrikerna i en belastningsutjämnad miljö som innefattar flera Image Serving-värdar. Klientcachning kan besegras och serverbelastningen ökar om servrarna av någon anledning har olika tidsstämplar för samma katalogposter. En sådan situation kan uppstå på följande sätt:
>
>* Varken `catalog::TimeStamp` eller `attribute::TimeStamp`, så att ändringstiden för filen [!DNL catalog.ini] används som standard för `catalog::TimeStamp`.
   >
   >
* I stället för att dela bildkatalogfilerna via ett nätverk har varje server en egen instans av katalogfilerna på ett lokalt filsystem.
>* Två eller flera förekomster av samma [!DNL catalog.ini]-fil har olika ändringsdatum, möjligen på grund av felaktig kopiering av filerna.

>



## Egenskaper {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Flagga. 0 för att inaktivera, 1 för att aktivera senast ändrade HTTP-huvuden.

## Standard {#section-4eb47aadab8b41609bef296a4115f9f4}

Ärvs från `default::UseLastModified` om det inte är definierat eller om det är tomt.

## Se även {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[katalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
