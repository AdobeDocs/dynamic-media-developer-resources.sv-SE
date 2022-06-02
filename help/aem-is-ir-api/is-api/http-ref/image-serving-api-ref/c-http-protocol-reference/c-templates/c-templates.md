---
title: Mallar
description: Mallar kan användas för att minska längden och komplexiteten hos förfrågningar som sammanställer flera bildlager eller som innehåller rtf-formaterad text.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Mallar{#templates}

Mallar kan användas för att minska längden och komplexiteten hos förfrågningar som sammanställer flera bildlager eller som innehåller rtf-formaterad text.

Anpassade variabler kan användas för att ytterligare förenkla mallanvändningen. Mallar är ofta inställda så att det blir enkelt att växla bilder eller text eller ange andra alternativ vid körning.

Mallar lagras som poster i bildkataloger, med malltexten i `catalog::Modifier` och `catalog::Path` fältet är tomt eller anger en statisk bakgrundsbild som inte kan ändras dynamiskt.

Mallar anges med `template=` eller i sökvägskomponenten för den begärda URL:en. För de flesta program bör du använda `template=` om du vill ange mallar. The `template=`-kommandot får inte finnas i `catalog::PostModifier` och kan bara förekomma i `catalog::Modifier` i en kapslad IS-begäran (dvs i en `src=is{...}` construct). Mallposter kan inte refereras i `src=` eller `mask=`kommandon.

Alla `src=` eller `mask=`kommandon som är inbäddade i mallen kan gå till huvudkatalogen för begäran eller till en annan bildkatalog. Om nej `rootId` anges explicit antas huvudkatalogen. Den mall som anges med `template=` kan också finnas i huvudkatalogen eller en annan bildkatalog.

Vi rekommenderar att du alltid inkluderar standarddefinitioner för alla variabler som används i en mall. På så sätt kan du alltid visa mallens bildutdata genom att ange dess `attribute::RootId` och `catalog::Id`utan att behöva veta vilka variabler som används i mallen.

Den fördefinierade variabeln för banersättning `$object$` kan användas för att tillämpa det bildobjekt som anges i url-banan på en lagerkälla eller mask ( `src=` eller `mask=`), även i kapslade eller inbäddade begäranden.

* [Exempel A](r-example-a.md)
* [Exempel B](r-example-b.md)
* [Exempel C](r-example-c.md)
