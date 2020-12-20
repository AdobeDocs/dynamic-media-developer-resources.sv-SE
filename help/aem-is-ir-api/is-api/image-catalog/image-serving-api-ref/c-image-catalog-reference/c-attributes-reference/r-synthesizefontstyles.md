---
description: Aktivera syntetiserade teckensnittsvarianter. Styr om servern ska generera ett felsvar eller syntetisera ett fet, kursivt eller fet/kursiv teckensnittsformat om en sådan stil begärs men inte kan hittas i teckensnittskartan.
seo-description: Aktivera syntetiserade teckensnittsvarianter. Styr om servern ska generera ett felsvar eller syntetisera ett fet, kursivt eller fet/kursiv teckensnittsformat om en sådan stil begärs men inte kan hittas i teckensnittskartan.
seo-title: SynthesizeFontStyles
solution: Experience Manager
title: SynthesizeFontStyles
topic: Scene7 Image Serving - Image Rendering API
uuid: f1c67490-7f14-4a6c-a7ba-5a476231ef34
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---


# SynthesizeFontStyles{#synthesizefontstyles}

Aktivera syntetiserade teckensnittsvarianter. Styr om servern ska generera ett felsvar eller syntetisera ett fet, kursivt eller fet/kursiv teckensnittsformat om en sådan stil begärs men inte kan hittas i teckensnittskartan.

>[!NOTE]
>
>Syntetisering av teckensnittsformat resulterar ofta i renderingar med lägre kvalitet än användning av faktiska teckensnitt för sådana format.

## Egenskaper {#section-3205560a74774ebf9c916b07bd15aca6}

Flagga. Ange 0 om du vill inaktivera och 1 om du vill aktivera syntetiska teckensnittsformat.

## Standard {#section-71f94aa65e404d14b441674c040b59e3}

Ärvs från `default::SynthesizeFontStyles` om det inte är definierat eller om det är tomt.

## Se även {#section-47a79659cc844272b6d5f36c946e12ac}

[Referens för teckensnittskarta](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
