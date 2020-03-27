---
description: Mellanliggande bilddata som skapas av kapslade/inbäddade bildserings- och bildåtergivningsbegäranden kan cachelagras genom att ange cache=on i den kapslade/inbäddade begäran. Dessa data lagras i ett specifikt format i svarsdatacachen.
seo-description: Mellanliggande bilddata som skapas av kapslade/inbäddade bildserings- och bildåtergivningsbegäranden kan cachelagras genom att ange cache=on i den kapslade/inbäddade begäran. Dessa data lagras i ett specifikt format i svarsdatacachen.
seo-title: Hjälpdatacache
solution: Experience Manager
title: Hjälpdatacache
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Hjälpdatacache{#auxiliary-data-caches}

Mellanliggande bilddata som skapas av kapslade/inbäddade bildserings- och bildåtergivningsbegäranden kan cachelagras genom att ange cache=on i den kapslade/inbäddade begäran. Dessa data lagras i ett specifikt format i svarsdatacachen.

Bilder som hämtas från externa HTTP-servrar lagras också i svarsdatacachen. Sådana bilder valideras automatiskt med valideringsverktyget innan cacheposten genereras.

Plattformsservern sammanställer bildkatalogdata för effektiv åtkomst. Dessa data lagras i `CS::CatalogCacheFolder`.
