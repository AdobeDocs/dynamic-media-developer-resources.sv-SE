---
description: Bildåtergivning använder material för grupper eller objekt i vinjetter.
solution: Experience Manager
title: Material
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Material{#materials}

Bildåtergivning använder material för grupper eller objekt i vinjetter.

Ett material består av en uppsättning *attribut*. Vissa attribut krävs för vissa material, andra är valfria och andra ignoreras om de finns. Många attribut har standardvärden. Alla material kan inte användas på alla objekt (t.ex. ett kabinettmaterial kan inte användas på en soffa).

Alla attribut som förekommer inom ett materialspecifikationssegment (MSS) men som varken anges ovan eller i de specifika materialtabellerna nedan ignoreras av servern.

I följande tabeller visas grundläggande materialattribut. IR har stöd för ytterligare attribut för styrning av [avancerade återgivningseffekter](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Om inget annat anges är alla materialattribut valfria, med lämpliga standardvärden.

* [Solida färger](r-ir-solid-colors.md)
* [Upprepningsbara texturer](r-ir-repeatable-textures.md)
* [Väggkanter](r-ir-wall-borders.md)
* [Decaler](r-ir-decals.md)
* [Skåp](r-ir-cabinets.md)
* [Fönsteromslag](r-ir-window-coverings.md)
