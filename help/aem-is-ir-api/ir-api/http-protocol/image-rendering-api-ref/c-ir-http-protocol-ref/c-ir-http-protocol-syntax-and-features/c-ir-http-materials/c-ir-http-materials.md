---
description: Bildåtergivning använder material för grupper eller objekt i vinjetter.
seo-description: Bildåtergivning använder material för grupper eller objekt i vinjetter.
seo-title: Material
solution: Experience Manager
title: Material
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '147'
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
