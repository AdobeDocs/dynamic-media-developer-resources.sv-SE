---
title: Material
description: Bildåtergivning använder material för grupper eller objekt i vinjetter.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Material{#materials}

Bildåtergivning använder material för grupper eller objekt i vinjetter.

Ett material består av en uppsättning *attribut*. Vissa attribut krävs för vissa material, andra är valfria och andra ignoreras om de finns. Många attribut har standardvärden. Alla material kan inte användas på alla objekt (ett kabinettmaterial kan till exempel inte användas på en soffa).

Alla attribut som förekommer inom ett materialspecifikationssegment (MSS) men som inte anges ovan eller i de specifika materialtabellerna nedan ignoreras av servern.

I följande tabeller visas grundläggande materialattribut. IR har stöd för ytterligare attribut för styrning av [avancerade återgivningseffekter](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Om inget annat anges är alla materialattribut valfria, med lämpliga standardvärden.

* [Solida färger](r-ir-solid-colors.md)
* [Upprepningsbara texturer](r-ir-repeatable-textures.md)
* [Väggkanter](r-ir-wall-borders.md)
* [Decaler](r-ir-decals.md)
* [Skåp](r-ir-cabinets.md)
* [Fönsteromslag](r-ir-window-coverings.md)
