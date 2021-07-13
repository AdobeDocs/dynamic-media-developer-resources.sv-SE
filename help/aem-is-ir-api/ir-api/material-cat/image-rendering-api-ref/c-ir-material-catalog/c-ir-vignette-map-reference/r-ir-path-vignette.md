---
description: Sökväg till vinjettfil. Relativ sökväg och namn för en vinjettfil.
solution: Experience Manager
title: Bana
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5562b0e0-0476-4dd0-acce-058601b9af0a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 1%

---

# Bana{#path}

Sökväg till vinjettfil. Relativ sökväg och namn för en vinjettfil.

Servern kombinerar det här värdet med `attribute::RootPath` för att skapa den faktiska filsökvägen för vinjettering. Kan också vara en absolut sökväg.

## Egenskaper {#section-b3b295feac084b56bd8a153c04987153}

Textsträng. Valfritt. Om det anges måste det vara en giltig relativ eller absolut filsökväg. Om den är tom måste `vignette::Modifier` innehålla kommandot `vignette=`.

## Standard {#section-a1d2133856084eb79a5be8230a4b38fd}

Ingen.

## Se även {#section-177131dad5804964bfb8957c1f6e5191}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
