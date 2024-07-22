---
description: Cacheposter uppdateras automatiskt med antingen katalogbaserad eller förfallobaserad cachevalidering, vilket väljs med attributet CacheValidationPolicy (i default.ini eller .ini-filen för en viss bildkatalog).
solution: Experience Manager
title: Verifiering av svarscache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Verifiering av svarscache{#response-cache-validation}

Cacheposter uppdateras automatiskt med antingen katalogbaserad eller förfallobaserad cachevalidering, enligt attributet::CacheValidationPolicy (i default.ini eller .ini-filen för en viss bildkatalog).

Med katalogbaserad validering betraktas en befintlig cachepost som inaktuell om `catalog::LastModified` (eller `attribute::LastModified`, eller om filändringstiden för filen [!DNL catalog.ini]) är senare än den tidpunkt då cacheposten skapades.

Med förfallobaserad validering blir en cachepost inaktuell efter 5 minuter sedan den senaste valideringen. I båda fallen validerar servern inaktuella cacheposter genom att kontrollera fildatumen för alla bildfiler som användes när begäran skapades. Om fildatumen inte har ändrats uppdateras tidsstämpeln för cacheposten och cachelagringsdatumet betraktas som giltigt.

För typiska program som till största delen innehåller bilder som är registrerade i bildkataloger ger ger katalogbaserad validering en prestandafördel. Program som inte innehåller bildkataloger bör använda förfallobaserad cachevalidering. Ett sätt att uppnå detta är att ange `attribute::cacheValidationPolicy=0` i [!DNL default.ini] och till `1` i alla specifika bildkatalogfiler.

Cacheposter blir ogiltiga och kan genereras om när en katalogpost som ingår i begäran ändras på ett sätt som troligen skulle orsaka en ändring av svarsbilden. Innehållet i `catalog::Modifier` ändras till exempel.

>[!NOTE]
>
>PTIFF-bilder (Dynamic Media pyramid TIFF) bevarar fildatumet internt i filhuvudet i valideringssyfte. Filändringstiden som bevaras av filsystemet används för att kontrollera om en fil som inte är en PTIFF-fil har ändrats.

Endast bildfiler deltar i cachevalideringsprocessen. Ändringar av teckensnittsfiler eller ICC-profilfiler medför inte att cacheposter ogiltigförklaras automatiskt.
