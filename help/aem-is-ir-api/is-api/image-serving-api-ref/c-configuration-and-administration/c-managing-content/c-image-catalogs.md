---
description: Bildkataloger innehåller många serverkonfigurationsinställningar, samt teckensnitt, ICC-profiler och kommandomakron.
solution: Experience Manager
title: Bildkataloger
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Bildkataloger{#image-catalogs}

Bildkataloger innehåller många serverkonfigurationsinställningar, samt teckensnitt, ICC-profiler och kommandomakron.

De mappar bild- och statiska innehålls-ID:n som används i begäranden till faktiska filsökvägar, lagrar olika bildmetadata, t.ex. bildscheman, och tillhandahåller behållare för mallar och bilduppsättningar.

Bildkataloger används endast av plattformsservern, aldrig av Image Server. Katalogattributfiler måste ha ett .ini-suffix och placeras i plattformsserverns katalogmapp ( `PS::CatalogFolder`). Minst standardbildkatalogen krävs och måste fyllas i med alla attribut för att plattformsservern ska fungera korrekt.
