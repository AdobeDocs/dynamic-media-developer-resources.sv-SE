---
description: Modifieringssträng för prefixbegäran. Inga eller flera bildserverkommandon avgränsade med "&"-tecken.
seo-description: Modifieringssträng för prefixbegäran. Inga eller flera bildserverkommandon avgränsade med "&"-tecken.
seo-title: Modifierare
solution: Experience Manager
title: Modifierare
topic: Dynamic Media Image Serving - Image Rendering API
uuid: eb17d115-22ec-4b1b-9039-9bd2bc256f48
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# Modifierare{#modifier}

Modifieringssträng för prefixbegäran. Inga eller flera bildserverkommandon avgränsade med &quot;&amp;&quot;-tecken.

Används för att permanent ändra bilder och lagra mallarna.

Kommandona i det här fältet åsidosätts av samma kommandon i den begäran eller mall som posten refereras till från, och av kommandon i `catalog::PostModifier`

Makron tillåts i `catalog::Modifier`, förutsatt att de definieras i samma katalog eller i standardkatalogen. Egna variabler kan också användas.

## Egenskaper {#section-6674388f77d644469371a17e8809c45f}

Textsträng. Valfritt.

## Standard {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Ingen.

## Se även {#section-7a67803d141b442180c418c1f3cff029}

[katalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
