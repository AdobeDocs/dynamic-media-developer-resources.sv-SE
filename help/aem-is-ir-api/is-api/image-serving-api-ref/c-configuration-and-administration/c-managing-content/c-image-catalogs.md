---
description: Bildkataloger innehåller många serverkonfigurationsinställningar, samt teckensnitt, ICC-profiler och kommandomakron.
seo-description: Bildkataloger innehåller många serverkonfigurationsinställningar, samt teckensnitt, ICC-profiler och kommandomakron.
seo-title: Bildkataloger
solution: Experience Manager
title: Bildkataloger
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Bildkataloger{#image-catalogs}

Bildkataloger innehåller många serverkonfigurationsinställningar, samt teckensnitt, ICC-profiler och kommandomakron.

De mappar bild- och statiska innehålls-ID:n som används i begäranden till faktiska filsökvägar, lagrar olika bildmetadata, t.ex. bildscheman, och tillhandahåller behållare för mallar och bilduppsättningar.

Bildkataloger används endast av plattformsservern, aldrig av Image Server. Katalogattributfiler måste ha ett .ini-suffix och placeras i plattformsserverns katalogmapp ( `PS::CatalogFolder`). Minst standardbildkatalogen krävs och måste fyllas i med alla attribut för att plattformsservern ska fungera korrekt.
