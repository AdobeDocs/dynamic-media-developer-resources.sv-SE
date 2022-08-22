---
title: RootPath
description: Källdatarotsökväg. Textsträngsvärde. Absolut sökväg eller relativt sökvägssegment för rotmappen för alla vinjett-, textur-, bild- och ICC-datafiler som refereras av den här bildkatalogen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# RootPath{#rootpath}

Källdatarotsökväg. Textsträngsvärde. Absolut sökväg eller relativt sökvägssegment för rotmappen för alla vinjett-, textur-, bild- och ICC-datafiler som refereras av den här bildkatalogen.

## Egenskaper {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Textsträng. Måste vara tomt, ett giltigt sökvägssegment i förhållande till serverkonfigurationsinställningen Bildåtergivning `ir.resourceRootPaths`eller en giltig absolut filsökväg. Bör inte innehålla inledande och avslutande sökvägselementavgränsare.

## Standard {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Ärvs från `default::RootPath` om inte definierat. Om den är definierad men tom, bidrar den inte till källfilens rotsökväg.

## Se även {#section-92012cc1ce32448ea977e7e0484857e2}

[katalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) , [katalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969), `ir.resourceRootPaths`
