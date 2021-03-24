---
description: Sökväg till datafil. Relativ sökväg och namn för datafiler som inte är bildfiler som är associerade med den här bilden.
solution: Experience Manager
title: AuxPath
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# AuxPath{#auxpath}

Sökväg till datafil. Relativ sökväg och namn för datafiler som inte är bildfiler som är associerade med den här bilden.

Servern kombinerar det här värdet med attributet::RootPath för att skapa den faktiska filsökvägen. Kan också vara en absolut filsökväg.

Används för att ange en kabinettformatfil för ett kabinettmaterial eller ett fönster som täcker en formatfil för ett fönster som täcker materialet. Lämna tomt för alla andra material.

## Egenskaper {#section-4268350054b7421da0ce0327f0731a52}

Textsträngsvärde. Om det anges måste det vara en giltig relativ eller absolut filsökväg. Krävs för kabinettmaterial och fönsterbeläggningsmaterial. Måste vara tomt för alla andra material.

## Standard {#section-287005c2d8e948fa958f69ba7b90b437}

Ingen.

## Se även {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
