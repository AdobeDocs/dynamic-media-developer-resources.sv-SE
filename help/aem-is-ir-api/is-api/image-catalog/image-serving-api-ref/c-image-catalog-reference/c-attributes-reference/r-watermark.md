---
description: Vattenstämpelväljare. Anger katalog-ID:t för katalogposten som ska användas som vattenstämpelbild eller mall.
seo-description: Vattenstämpelväljare. Anger katalog-ID:t för katalogposten som ska användas som vattenstämpelbild eller mall.
seo-title: Vattenstämpel
solution: Experience Manager
title: Vattenstämpel
topic: Scene7 Image Serving - Image Rendering API
uuid: 18add7ab-0797-4ab3-a7e8-05c745abe605
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# Vattenstämpel{#watermark}

Vattenstämpelväljare. Anger katalogen::Id för den katalogpost som ska användas som vattenstämpelbild eller mall.

Om det anges använder servern vattenstämpeln på de begärda bilddata för alla bildbegäranden ( `req=img`).

## Egenskaper {#section-fad6ffff4c5f4b5c8010281bc1377055}

Textsträng. Om det anges måste det vara ett giltigt `Catalog::Id` värde i den här bildkatalogen (eller i standardkatalogen, om det anges i [!DNL default.ini]).

## Standard {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Ärvs från `default::Watermark` om inte definierat. Om den är definierad men tom används ingen vattenstämpel för den här bildkatalogen, även om `default::Watermark` den är definierad.

## Se även {#section-f15dbe31013849828d78588742dde58e}

[katalog::ID](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
