---
description: Aktivera senaste ändrade svarshuvuden. Aktiverar eller inaktiverar inkludering av den senast ändrade rubriken i tillgängliga HTTP-svar som genereras av bildåtergivning.
seo-description: Aktivera senaste ändrade svarshuvuden. Aktiverar eller inaktiverar inkludering av den senast ändrade rubriken i tillgängliga HTTP-svar som genereras av bildåtergivning.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# UseLastModified{#uselastmodified}

Aktivera senaste ändrade svarshuvuden. Aktiverar eller inaktiverar inkludering av den senast ändrade rubriken i tillgängliga HTTP-svar som genereras av bildåtergivning.

Servern använder det senaste `vignette::TimeStamp`- och `catalog::TimeStamp`-värdet för alla vinjett- och materialkataloger/kataloger som ingår i ett svar som det senast ändrade rubrikvärdet.

Bör bara aktiveras om ett distribuerat cachelagringsnätverk, t.ex. Akamai, används som inte har stöd för tagghuvuden.

>[!NOTE]
>
>Försiktighet måste iakttas när du använder de senast ändrade rubrikerna i en belastningsutjämnad miljö som innefattar flera Image Serving/Rendering-värdar. Klientcachning kan besegras och serverbelastningen ökar om servrarna av någon anledning har olika tidsstämplar för samma katalogposter. En sådan situation kan uppstå på följande sätt:

* Varken `catalog::TimeStamp`, `vignette::TimeStamp` eller `attribute::TimeStamp` har definierats så att ändringstiden för [!DNL catalog.ini]-filen används som standard för `catalog::TimeStamp`.

* I stället för att dela materialkatalogfilerna via ett nätverk har varje server en egen instans av katalogfilerna på ett lokalt filsystem.
* Två eller flera förekomster av samma [!DNL catalog.ini]-fil har olika ändringsdatum, möjligen på grund av felaktig kopiering av filerna.

## Egenskaper {#section-453952244193452caccfaf7f601007c1}

Flagga. 0 för att inaktivera, 1 för att aktivera senast ändrade HTTP-huvuden.

## Standard {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Ärvs från `default::UseLastModified` om det inte är definierat eller om det är tomt.

## Se även {#section-1536715169da48b0aecc4ab7326c86db}

[katalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vinjettering::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
