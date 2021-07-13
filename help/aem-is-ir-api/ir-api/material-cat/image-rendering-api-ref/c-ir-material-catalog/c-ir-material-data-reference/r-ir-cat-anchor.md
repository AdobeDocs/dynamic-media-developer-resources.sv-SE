---
description: Bildankarpunkt. Anger fästpunkten (hotspot) för en repeterbar textur, väggkant eller dekal bild.
solution: Experience Manager
title: Ankarpunkt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Ankarpunkt{#anchor}

Bildankarpunkt. Anger fästpunkten (hotspot) för en repeterbar textur, väggkant eller dekal bild.

En upprepningsbar textur används på ett vinjetteringsobjekt så att texturankarpunkten finns vid objektets texturstartpunkt. En dekal bild används på ett vinjetteringsobjekt så att den dekala fästpunkten finns vid objektets dekala utgångspunkt. För vägggränser används endast x-värdet. y-värdet ignoreras.

## Egenskaper {#section-bc4bc8b897c64535b88681e57d72942f}

Två heltal avgränsade med kommatecken. Pixelförskjutning i förhållande till bildens övre vänstra hörn. Ignoreras om `catalog::Alignment=3` och av heltäckande färg och kabinettmaterial.

## Standard {#section-b7ccc419a356415294706cd295ae96c9}

Om fältet är tomt eller inte finns, används bildens övre vänstra hörn (0,0) för repeterbara texturmaterial, eller bildens mittpunkt om det är dekala material.

## Se även {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[katalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
