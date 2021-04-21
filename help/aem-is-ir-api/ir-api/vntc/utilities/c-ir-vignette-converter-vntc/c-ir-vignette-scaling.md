---
description: Fyra allmänna typer av produktionsvinjettering stöds.
solution: Experience Manager
title: Skalning av vinjettering
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---


# Skalning av vinjettering{#vignette-scaling}

Fyra allmänna typer av produktionsvinjettering stöds.

* Enkelupplösning

   Rekommenderas endast när det är säkert att endast en renderingsbildstorlek krävs.
* Flera upplösningar

   Rekommenderas när alla önskade bildstorlekar för återgivning är kända. Ger bättre kvalitet och snabbare återgivning än enupplösning- och pyramidvinjettering eftersom bilden inte behöver skalas efter återgivningen.
* Pyramid

   Bäst för alla syften, som rekommenderas när flera bildstorlekar behövs och de exakta storlekarna inte är förbestämda och när visningsprogrammet för Dynamic Media Zoom används.
* Pyramid med en eller flera upplösningar

   Ger hög kvalitet för specifika storlekar samtidigt som stöd för visningsprogram för zoomning och flexibilitet bibehålls.

I praktiken sparas varje upplösning i produktionsvinjetteringen som en oberoende vy med sin egen bildbredd och -höjd.

Vystorleken för en enupplöst vinjett anges med antingen `-width` eller `-height` eller båda. Om båda värdena anges skalförändras vinjetteringen så att ingen dimension är större än den angivna storleken. Om inget av värdena anges får utdatavvinjetteringen samma storlek som indatavvinjetteringen. Ingen uppskalning kommer att tillämpas. Om den angivna storleken är större än storleken på indatavvinjetteringen får utdatavvinjetteringen samma storlek som indatavvinjetteringen.

Samma regler gäller för flerupplösta vinjetter, där den första upplösningsnivån storleksändras precis som en vinjettering med en upplösning. Ytterligare upplösningar anges med ytterligare kommaavgränsade värden för antingen `-width` eller `-height`. Värden behöver inte sorteras. Om `-width` anger flera värden får `-height` bara ange ett enda värde, och vice versa, annars returneras ett fel.

En pyramidvinjettering skapas genom att ange `-pyramid`. Den största upplösningsnivån för en sådan vinjett bestäms exakt som för en vinjett med en upplösning. De extra upplösningsnivåerna bestäms automatiskt genom att varje nivå skalas till 0,5 gånger föregående nivå, med den minsta nivån som inte överstiger 128 x 128 pixlar.

Ytterligare upplösningsnivåer kan anges för en pyramidvinjettering, precis som för en vinjett med flera upplösningar.
