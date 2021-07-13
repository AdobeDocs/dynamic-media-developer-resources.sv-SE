---
description: Mellanliggande bilddata som skapas av kapslade/inbäddade bildserings- och bildåtergivningsbegäranden kan cachelagras genom att ange cache=on i den kapslade/inbäddade begäran. Dessa data lagras i ett specifikt format i svarsdatacachen.
solution: Experience Manager
title: Hjälpdatacache
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Hjälpdatacache{#auxiliary-data-caches}

Mellanliggande bilddata som skapas av kapslade/inbäddade bildserings- och bildåtergivningsbegäranden kan cachelagras genom att ange cache=on i den kapslade/inbäddade begäran. Dessa data lagras i ett specifikt format i svarsdatacachen.

Bilder som hämtas från externa HTTP-servrar lagras också i svarsdatacachen. Sådana bilder valideras automatiskt med valideringsverktyget innan cacheposten genereras.

Plattformsservern sammanställer bildkatalogdata för effektiv åtkomst. Dessa data lagras i `CS::CatalogCacheFolder`.
