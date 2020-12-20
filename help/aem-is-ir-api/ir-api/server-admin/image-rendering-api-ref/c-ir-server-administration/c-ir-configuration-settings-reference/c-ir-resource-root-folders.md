---
description: Lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.
seo-description: Lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.
seo-title: Resursrotmappar (ir.resourceRootPaths)
solution: Experience Manager
title: Resursrotmappar (ir.resourceRootPaths)
topic: Scene7 Image Serving - Image Rendering API
uuid: a2a8ecd1-ddfe-46c5-bb70-4640e0992de8
translation-type: tm+mt
source-git-commit: 2bc6fe0369808990642cf7afdccff647c48260d9
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# Resursrotmappar (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.

Kan antingen vara absoluta sökvägar eller sökvägar i förhållande till *[!DNL install_folder]*. När flera sökvägar har angetts provar servern varje rot i den angivna ordningen tills filen hittas. Standardvärdet är [!DNL ./resources], för standardrotsökvägen [!DNL install_folder/resources].
