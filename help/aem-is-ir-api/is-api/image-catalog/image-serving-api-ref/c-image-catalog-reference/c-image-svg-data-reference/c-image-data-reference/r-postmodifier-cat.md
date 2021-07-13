---
description: Modifieringssträng för postfix-begäran. Inga eller flera bildserverkommandon avgränsade med "&"-tecken.
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '132'
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
