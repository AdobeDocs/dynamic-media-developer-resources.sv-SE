---
title: Teckensnittshantering
description: Alla teckensnitt som refereras i RTF-strängen måste vara tillgängliga i teckensnittsmappningsfilen för standardkatalogen eller den aktuella bildkatalogen, annars returneras ett fel.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e8e3ce9850ab8059aed81e720574d0c93f867a22
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---

# Teckensnittshantering{#font-handling}

Alla teckensnitt som refereras i RTF-strängen måste vara tillgängliga i teckensnittsmappningsfilen för standardkatalogen eller den aktuella bildkatalogen, annars returneras ett fel.

Du får bäst kvalitet på kursiv och fet stil om du registrerar motsvarande teckensnittsfiler. Om den inte är tillgänglig kan servern syntetisera feta och/eller kursiva teckensnitt från standardteckensnittet. (Se [attribute::SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

Teckensnittet som anges med `attribute::DefaultFont` används när ingen anges explicit i RTF-strängen.

Image Serving har stöd för TrueType, OpenType® och Adobe Type 1 (endast Windows).

<!-- THIS APPEARS TO BE VERY OLD OUTDATED INFORMATION; URL IS DEAD TOO ## Photofont&reg; font support {#section-74560ae898cf4708aba4c8b4093f5f00}

Photofont&reg; fonts support `textPs=`, with the following restrictions:

* `\cf` is ignored in text spans that specify a Photofont font; Photofont font faces have predefined colors 
* Synthesized font styles are not supported; use of `\b` and `\i`require corresponding font map entries, otherwise an error is returned 

* Vertical text flow is not supported 
* Photofont fonts with 16-bit images are not supported 
* Photofont fonts with multiple glyphs per image are not supported 
* Naïve color conversion is applied unless the Photofont glyph images embed color profiles; in this case, relative colorimetric render intent and blackpoint compensation are always applied

See [https://www.photofont.com](https://www.photofont.com) for additional information. -->

## Se även {#section-6cb8a802aa044836bbe449d559093f3a}

[Referens för teckensnittskarta](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribut::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)
