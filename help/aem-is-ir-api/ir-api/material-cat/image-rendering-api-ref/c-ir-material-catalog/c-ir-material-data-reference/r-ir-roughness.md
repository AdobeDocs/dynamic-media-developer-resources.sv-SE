---
description: Ytojämnhet. Anger materialytans relativa glansighet. Används tillsammans med katalogtyp och katalogglans för att styra återgivningseffekter för 3D-reflektion.
seo-description: Ytojämnhet. Anger materialytans relativa glansighet. Används tillsammans med katalogtyp och katalogglans för att styra återgivningseffekter för 3D-reflektion.
seo-title: Grovhet
solution: Experience Manager
title: Grovhet
topic: Scene7 Image Serving - Image Rendering API
uuid: d71e4411-dd59-4347-a7c2-132e130ff36b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Grovhet{#roughness}

Ytojämnhet. Anger materialytans relativa glansighet. Används tillsammans med katalog::Type och katalog::Gloss för att styra återgivningseffekter för 3D-reflektion.

## Egenskaper {#section-70c3f2394fd8477ca83a369448907971}

Heltal. Procentvärde i intervallet 0 till 100. Valfritt för alla material. Används endast för vinjetter med flera reflektionskartor eller vinjetter med 3D-reflektion. Lämna tomt eller ange -1 om det inte är känt eller inte behövs.

## Standard {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; används en serverstandard.

## Se även {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[grov=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [katalog::Glans](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [katalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
