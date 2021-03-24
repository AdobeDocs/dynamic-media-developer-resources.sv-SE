---
description: Mellanliggande bilddata som skapas av kapslade/inbäddade bildserings- och bildåtergivningsbegäranden kan cachelagras genom att ange cache=on i den kapslade/inbäddade begäran. Dessa data lagras i ett specifikt format i svarsdatacachen.
solution: Experience Manager
title: Hjälpdatacache
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# Hjälpdatacache{#auxiliary-data-caches}

Mellanliggande bilddata som skapas av kapslade/inbäddade bildserings- och bildåtergivningsbegäranden kan cachelagras genom att ange cache=on i den kapslade/inbäddade begäran. Dessa data lagras i ett specifikt format i svarsdatacachen.

Bilder som hämtas från externa HTTP-servrar lagras också i svarsdatacachen. Sådana bilder valideras automatiskt med valideringsverktyget innan cacheposten genereras.

Plattformsservern sammanställer bildkatalogdata för effektiv åtkomst. Dessa data lagras i `CS::CatalogCacheFolder`.
