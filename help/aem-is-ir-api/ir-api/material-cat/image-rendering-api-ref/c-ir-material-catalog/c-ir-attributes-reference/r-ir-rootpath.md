---
description: Källdatarotsökväg. Textsträngsvärde. Absolut sökväg eller relativt sökvägssegment för rotmappen för alla vinjett-, textur-, bild- och ICC-datafiler som refereras av den här bildkatalogen.
seo-description: Källdatarotsökväg. Textsträngsvärde. Absolut sökväg eller relativt sökvägssegment för rotmappen för alla vinjett-, textur-, bild- och ICC-datafiler som refereras av den här bildkatalogen.
seo-title: RootPath *
solution: Experience Manager
title: RootPath *
topic: Scene7 Image Serving - Image Rendering API
uuid: a23ea524-8ca4-47c4-83a5-64a174d8767e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# RootPath *{#rootpath}

Källdatarotsökväg. Textsträngsvärde. Absolut sökväg eller relativt sökvägssegment för rotmappen för alla vinjett-, textur-, bild- och ICC-datafiler som refereras av den här bildkatalogen.

## Egenskaper {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Textsträng. Måste vara tomt, ett giltigt sökvägssegment relativt serverkonfigurationsinställningen Bildåtergivning `ir.resourceRootPaths`eller en giltig absolut sökväg. Bör inte innehålla inledande och avslutande sökvägselementavgränsare.

## Standard {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Ärvs från `default::RootPath` om inte definierat. Om den är definierad men tom, kommer inte att bidra till källfilens rotsökväg.

## Se även {#section-92012cc1ce32448ea977e7e0484857e2}

[katalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) , [katalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969), `ir.resourceRootPaths`
