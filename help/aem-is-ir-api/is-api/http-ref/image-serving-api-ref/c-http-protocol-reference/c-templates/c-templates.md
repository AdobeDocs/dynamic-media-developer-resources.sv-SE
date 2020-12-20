---
description: Mallar kan användas för att minska längden och komplexiteten hos förfrågningar som sammanställer flera bildlager eller som innehåller rtf-formaterad text.
seo-description: Mallar kan användas för att minska längden och komplexiteten hos förfrågningar som sammanställer flera bildlager eller som innehåller rtf-formaterad text.
seo-title: Mallar
solution: Experience Manager
title: Mallar
topic: Scene7 Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---


# Mallar{#templates}

Mallar kan användas för att minska längden och komplexiteten hos förfrågningar som sammanställer flera bildlager eller som innehåller rtf-formaterad text.

Anpassade variabler kan användas för att ytterligare förenkla mallanvändningen. Mallar är ofta inställda så att det blir enkelt att växla bilder eller text eller ange andra alternativ vid körning.

Mallar lagras som poster i bildkataloger, med malltexten i fältet `catalog::Modifier` och fältet `catalog::Path` tomt eller ange en statisk bakgrundsbild som inte kan ändras dynamiskt.

Mallar anges med kommandot `template=` eller i sökvägskomponenten i URL:en för begäran. För de flesta program bör du använda kommandot `template=` för att ange mallar. Kommandot `template=`får inte förekomma i fältet `catalog::PostModifier` och får bara förekomma i fältet `catalog::Modifier` i en kapslad IS-begäran (d.v.s. i en `src=is{...}`-konstruktion). Mallposter kan inte refereras i `src=`- eller `mask=`kommandon.

Alla `src=`- eller `mask=`kommandon som är inbäddade i mallen kan gå till huvudkatalogen för begäran eller till en annan bildkatalog. Om ingen `rootId` anges explicit antas huvudkatalogen. Mallen som anges med `template=` kan också finnas i huvudkatalogen eller en annan bildkatalog.

Vi rekommenderar att du alltid inkluderar standarddefinitioner för alla variabler som används i en mall. På så sätt kan du alltid visa mallens bildutdata genom att ange dess `attribute::RootId` och `catalog::Id`, utan att behöva veta vilka variabler som används i mallen.

Den fördefinierade variabeln `$object$` för banersättning kan användas för att tillämpa det bildobjekt som anges i url-sökvägen på en lagerkälla eller mask ( `src=` eller `mask=`), även i kapslade eller inbäddade begäranden.

* [Exempel A](r-example-a.md)
* [Exempel B](r-example-b.md)
* [Exempel C](r-example-c.md)
