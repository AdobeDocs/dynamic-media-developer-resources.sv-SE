---
description: Cacheposter uppdateras automatiskt med antingen katalogbaserad eller förfallobaserad cachevalidering, vilket väljs med attributet CacheValidationPolicy (i default.ini eller .ini-filen för en viss bildkatalog).
seo-description: Cacheposter uppdateras automatiskt med antingen katalogbaserad eller förfallobaserad cachevalidering, vilket väljs med attributet CacheValidationPolicy (i default.ini eller .ini-filen för en viss bildkatalog).
seo-title: Verifiering av svarscache
solution: Experience Manager
title: Verifiering av svarscache
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# Verifiering av svarscache{#response-cache-validation}

Cacheposter uppdateras automatiskt med antingen katalogbaserad eller förfallobaserad cachevalidering, enligt attributet::CacheValidationPolicy (i default.ini eller .ini-filen för en viss bildkatalog).

Med katalogbaserad validering betraktas en befintlig cachepost som inaktuell om `catalog::LastModified` (eller `attribute::LastModified`, eller om filändringstiden för [!DNL catalog.ini]-filen) är senare än den tidpunkt då cacheposten skapades.

Med förfallobaserad validering blir en cachepost inaktuell efter 5 minuter sedan den senaste valideringen. I båda fallen validerar servern inaktuella cacheposter genom att kontrollera fildatumen för alla bildfiler som användes när begäran skapades. Om fildatumen inte har ändrats uppdateras tidsstämpeln för cacheposten och cachelagringsdatumet betraktas som giltigt.

För typiska program som till största delen innehåller bilder som är registrerade i bildkataloger ger ger katalogbaserad validering en prestandafördel. Program som inte innehåller bildkataloger bör använda förfallobaserad cachevalidering. Ett sätt att uppnå detta är att ange `attribute::cacheValidationPolicy=0` i [!DNL default.ini] och till `1` i alla specifika bildkatalogfiler.

Cacheposter blir ogiltiga och kan genereras om när en katalogpost som ingår i begäran ändras på ett sätt som troligen skulle orsaka en ändring av svarsbilden. Innehållet i `catalog::Modifier` ändras till exempel.

>[!NOTE]
>
>Dynamic Media pyramid TIFF-bilder (PTIFF) bevarar fildatumet internt i filhuvudet för valideringsändamål. Filändringstiden som bevaras av filsystemet används för att kontrollera om en fil som inte är en PTIFF-fil har ändrats.

Endast bildfiler deltar i cachevalideringsprocessen. Ändringar av teckensnittsfiler eller ICC-profilfiler medför inte att cacheposter ogiltigförklaras automatiskt.
