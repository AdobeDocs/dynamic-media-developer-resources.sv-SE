---
description: Rotsökväg för statiska innehållsdata. Absolut sökväg eller relativt sökvägssegment för rotmappen för statiska innehållsdata i den här bildkatalogen.
solution: Experience Manager
title: StaticContentRootPath
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# StaticContentRootPath{#staticcontentrootpath}

Rotsökväg för statiska innehållsdata. Absolut sökväg eller relativt sökvägssegment för rotmappen för statiska innehållsdata i den här bildkatalogen.

Mer information om serverrotsökvägar finns i [Hantera källdata](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173).

## Egenskaper {#section-f8e3986096294b36948d43aafdc3e795}

Textsträng. Måste vara tom, ett giltigt relativt filsökvägssegment eller en absolut sökväg. Bör inte innehålla inledande och avslutande sökvägselementavgränsare.

## Standard {#section-0f741f90fd8d4758a43162c2b5c8a3a3}

Ärvs från `default::StaticContentsRootPath` om inte definierat. Om den är definierad men tom, kommer inte att bidra till källfilens rotsökväg.

## Se även {#section-9af8846d20d242789df67877f84ed8a7}

[PS::staticContent.rootPaths](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-staticcontentrootpath.md#reference-a2b5368d078349828d282357681bb2a5) ,   [hantera källdata](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)
