---
description: Modifieringssträng för prefixbegäran. Inga eller flera bildserverkommandon avgränsade med "&"-tecken.
solution: Experience Manager
title: Modifierare
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# Modifierare{#modifier}

Modifieringssträng för prefixbegäran. Inga eller flera bildserverkommandon avgränsade med &quot;&amp;&quot;-tecken.

Används för att permanent ändra bilder och lagra mallarna.

Kommandona i det här fältet åsidosätts av samma kommandon i den begäran eller mall som posten refereras till från, samt av kommandon i `catalog::PostModifier`

Makron tillåts i `catalog::Modifier`, förutsatt att de är definierade i samma katalog eller i standardkatalogen. Egna variabler kan också användas.

## Egenskaper {#section-6674388f77d644469371a17e8809c45f}

Textsträng. Valfritt.

## Standard {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Ingen.

## Se även {#section-7a67803d141b442180c418c1f3cff029}

[katalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
