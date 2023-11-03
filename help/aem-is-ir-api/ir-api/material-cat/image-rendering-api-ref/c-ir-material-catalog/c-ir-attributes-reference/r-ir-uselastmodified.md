---
title: UseLastModified
description: Aktivera senaste ändrade svarshuvuden. Aktiverar eller inaktiverar inkludering av den senast ändrade rubriken i tillgängliga HTTP-svar som genereras av bildåtergivning.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# UseLastModified{#uselastmodified}

Aktivera senaste ändrade svarshuvuden. Aktiverar eller inaktiverar inkludering av den senast ändrade rubriken i tillgängliga HTTP-svar som genereras av bildåtergivning.

Servern använder den senaste `vignette::TimeStamp` och `catalog::TimeStamp` värdet för alla vinjett- och materialkataloger/katalogposter som ingår i ett svar som rubrikvärdet Senaste ändring.

Bör bara aktiveras om ett distribuerat cachelagringsnätverk, t.ex. Akamai, används som inte har stöd för taggrubriker.

>[!NOTE]
>
>Försiktighet måste iakttas när du använder de senast ändrade rubrikerna i en belastningsutjämnad miljö som omfattar flera Image Serving/Rendering-värdar. Klientcachning kan besegras och serverbelastningen ökar om servrarna av någon anledning har olika tidsstämplar för samma katalogposter. En sådan situation kan uppstå på följande sätt:

* `catalog::TimeStamp`, `vignette::TimeStamp`, eller `attribute::TimeStamp` är inte definierad så att ändringstiden för [!DNL catalog.ini] används som standard för `catalog::TimeStamp`.

* I stället för att dela materialkatalogfilerna via en nätverksmontering har varje server en egen instans av katalogfilerna på ett lokalt filsystem.
* Två eller flera instanser av samma [!DNL catalog.ini] filen har olika ändringsdatum, vilket kan bero på felaktig kopiering av filerna.

## Egenskaper {#section-453952244193452caccfaf7f601007c1}

Flagga. 0 för att inaktivera, 1 för att aktivera senast ändrade HTTP-huvuden.

## Standard {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Ärvs från `default::UseLastModified` om den inte är definierad eller om den är tom.

## Se även {#section-1536715169da48b0aecc4ab7326c86db}

[katalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vinjett::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
