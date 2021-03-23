---
description: Mellanliggande bilddata som skapas av kapslade/inbäddade bildserings- och bildåtergivningsbegäranden kan cachelagras genom att ange cache=on i den kapslade/inbäddade begäran. Dessa data lagras i ett specifikt format i svarsdatacachen.
seo-description: Mellanliggande bilddata som skapas av kapslade/inbäddade bildserings- och bildåtergivningsbegäranden kan cachelagras genom att ange cache=on i den kapslade/inbäddade begäran. Dessa data lagras i ett specifikt format i svarsdatacachen.
seo-title: Hjälpdatacache
solution: Experience Manager
title: Hjälpdatacache
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Hjälpdatacache{#auxiliary-data-caches}

Mellanliggande bilddata som skapas av kapslade/inbäddade bildserings- och bildåtergivningsbegäranden kan cachelagras genom att ange cache=on i den kapslade/inbäddade begäran. Dessa data lagras i ett specifikt format i svarsdatacachen.

Bilder som hämtas från externa HTTP-servrar lagras också i svarsdatacachen. Sådana bilder valideras automatiskt med valideringsverktyget innan cacheposten genereras.

Plattformsservern sammanställer bildkatalogdata för effektiv åtkomst. Dessa data lagras i `CS::CatalogCacheFolder`.
