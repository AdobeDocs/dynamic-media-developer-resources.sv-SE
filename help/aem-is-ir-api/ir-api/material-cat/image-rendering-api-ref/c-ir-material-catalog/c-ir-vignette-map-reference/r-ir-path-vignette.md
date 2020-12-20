---
description: Sökväg till vinjettfil. Relativ sökväg och namn för en vinjettfil.
seo-description: Sökväg till vinjettfil. Relativ sökväg och namn för en vinjettfil.
seo-title: Bana
solution: Experience Manager
title: Bana
topic: Scene7 Image Serving - Image Rendering API
uuid: 470cee37-9840-402a-bde5-ace8988996d2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---


# Sökväg{#path}

Sökväg till vinjettfil. Relativ sökväg och namn för en vinjettfil.

Servern kombinerar det här värdet med `attribute::RootPath` för att skapa den faktiska filsökvägen för vinjettering. Kan också vara en absolut sökväg.

## Egenskaper {#section-b3b295feac084b56bd8a153c04987153}

Textsträng. Valfritt. Om det anges måste det vara en giltig relativ eller absolut filsökväg. Om den är tom måste `vignette::Modifier` innehålla kommandot `vignette=`.

## Standard {#section-a1d2133856084eb79a5be8230a4b38fd}

Ingen.

## Se även {#section-177131dad5804964bfb8957c1f6e5191}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
