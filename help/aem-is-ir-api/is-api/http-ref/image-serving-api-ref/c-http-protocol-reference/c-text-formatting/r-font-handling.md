---
description: Alla teckensnitt som refereras i RTF-strängen måste vara tillgängliga i teckensnittsmappningsfilen för standardkatalogen eller den aktuella bildkatalogen, annars returneras ett fel.
seo-description: Alla teckensnitt som refereras i RTF-strängen måste vara tillgängliga i teckensnittsmappningsfilen för standardkatalogen eller den aktuella bildkatalogen, annars returneras ett fel.
seo-title: Teckensnittshantering
solution: Experience Manager
title: Teckensnittshantering
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Teckensnittshantering{#font-handling}

Alla teckensnitt som refereras i RTF-strängen måste vara tillgängliga i teckensnittsmappningsfilen för standardkatalogen eller den aktuella bildkatalogen, annars returneras ett fel.

Du får bäst kvalitet på kursiv och fet stil om du registrerar motsvarande teckensnittsfiler. Om den inte är tillgänglig kan servern syntetisera feta och/eller kursiva teckensnitt från standardteckensnittet. (Se ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

Teckensnittet som anges med `attribute::DefaultFont` används när ingen anges explicit i RTF-strängen.

Image Serving har stöd för TrueType-, OpenType- och Adobe Type 1-teckensnitt (endast Windows).

## Stöd för teckensnitt i Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` stöder Photofont®-teckensnitt med följande begränsningar:

* `\cf` ignoreras i textintervall där teckensnittet Photofont anges, Teckensnittet i Photoshop har fördefinierade färger
* Syntetiserade teckensnittsformat stöds inte. användning `\b` och `\i`kräver motsvarande teckensnittsmappningsposter, annars returneras ett fel

* Lodrätt textflöde stöds inte
* Fototeckensnitt med 16-bitarsbilder stöds inte
* Fototeckensnitt med flera tecken per bild stöds inte
* Tidigare färgkonvertering används om inte färgprofiler bäddas in i fototeckensnittsbilder. i det här fallet används alltid den relativa färgorimetriska återgivningsmetoden och svartpunktskompensationen

Mer information finns ` [www.photofont.com](http://www.photofont.com)` i.

## Se även {#section-6cb8a802aa044836bbe449d559093f3a}

[Referens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)för teckensnittskarta, [attribut::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribut::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](http://www.photofont.com)
