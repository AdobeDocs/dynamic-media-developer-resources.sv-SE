---
description: Bildkataloger innehåller många serverkonfigurationsinställningar, samt teckensnitt, ICC-profiler och kommandomakron.
solution: Experience Manager
title: Bildkataloger
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Bildkataloger{#image-catalogs}

Bildkataloger innehåller många serverkonfigurationsinställningar, samt teckensnitt, ICC-profiler och kommandomakron.

De mappar bild- och statiska innehålls-ID:n som används i begäranden till faktiska filsökvägar, lagrar olika bildmetadata, t.ex. bildscheman, och tillhandahåller behållare för mallar och bilduppsättningar.

Bildkataloger används endast av plattformsservern, aldrig av Image Server. Katalogattributfiler måste ha ett .ini-suffix och placeras i plattformsserverns katalogmapp ( `PS::CatalogFolder`). Minst standardbildkatalogen krävs och måste fyllas i med alla attribut för att plattformsservern ska fungera korrekt.
