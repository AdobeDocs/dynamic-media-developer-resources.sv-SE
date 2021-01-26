---
description: Modifieringssträng för postfix-begäran. Inga eller flera bildserverkommandon avgränsade med "&"-tecken.
seo-description: Modifieringssträng för postfix-begäran. Inga eller flera bildserverkommandon avgränsade med "&"-tecken.
seo-title: PostModifier
solution: Experience Manager
title: PostModifier
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---


# PostModifier{#postmodifier}

Modifieringssträng för postfix-begäran. Inga eller flera bildserverkommandon avgränsade med &quot;&amp;&quot;-tecken.

Kommandon i det här fältet åsidosätter alltid kommandon i HTTP-begäran och i `catalog::Modifier`.

`catalog::PostModifier` är användbart om vissa bilder kräver särskilda inställningar som normalt styrs från URL-adressen, till exempel  `qlt=` eller  `resmode=`. `catalog::Modifier` ska användas för att ange de flesta IS-kommandon i bildkatalogen.

Makron tillåts i `catalog::PostModifier`, förutsatt att de definieras i samma katalog eller i standardkatalogen. Egna variabler kan också användas.

>[!NOTE]
>
>Om en begäran innehåller flera lager används endast innehållet i `catalog::PostModifier` för lager 0. `catalog::PostModifier` av alla andra lager ignoreras.

## Egenskaper {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Textsträng. Valfritt.

## Standard {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Ingen.

## Se även {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[katalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
