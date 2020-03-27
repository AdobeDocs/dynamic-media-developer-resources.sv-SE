---
description: Bildankarpunkt. Anger fästpunkten (hotspot) för en repeterbar textur, väggkant eller dekal bild.
seo-description: Bildankarpunkt. Anger fästpunkten (hotspot) för en repeterbar textur, väggkant eller dekal bild.
seo-title: Ankarpunkt
solution: Experience Manager
title: Ankarpunkt
topic: Scene7 Image Serving - Image Rendering API
uuid: 0b1a0fea-b299-44dc-b9fd-5916130b2ef3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ankarpunkt{#anchor}

Bildankarpunkt. Anger fästpunkten (hotspot) för en repeterbar textur, väggkant eller dekal bild.

En upprepningsbar textur används på ett vinjetteringsobjekt så att texturankarpunkten finns vid objektets texturstartpunkt. En dekal bild används på ett vinjetteringsobjekt så att den dekala fästpunkten finns vid objektets dekala utgångspunkt. För vägggränser används endast x-värdet. y-värdet ignoreras.

## Egenskaper {#section-bc4bc8b897c64535b88681e57d72942f}

Två heltal avgränsade med kommatecken. Pixelförskjutning i förhållande till bildens övre vänstra hörn. Ignoreras om `catalog::Alignment=3` och med heltäckande färg och kabinettmaterial.

## Standard {#section-b7ccc419a356415294706cd295ae96c9}

Om fältet är tomt eller inte finns, används bildens övre vänstra hörn (0,0) för repeterbara texturmaterial, eller bildens mittpunkt om det är dekala material.

## Se även {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[katalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
