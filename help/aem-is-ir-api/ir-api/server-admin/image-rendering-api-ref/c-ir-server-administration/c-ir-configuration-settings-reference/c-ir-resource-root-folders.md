---
description: Lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.
seo-description: Lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.
seo-title: Resursrotmappar (ir.resourceRootPaths)
solution: Experience Manager
title: Resursrotmappar (ir.resourceRootPaths)
uuid: a2a8ecd1-ddfe-46c5-bb70-4640e0992de8
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Resursrotmappar (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.

Kan antingen vara absoluta sökvägar eller sökvägar i förhållande till *[!DNL install_folder]*. När flera sökvägar har angetts provar servern varje rot i den angivna ordningen tills filen hittas. Standardvärdet är [!DNL ./resources], för standardrotsökvägen [!DNL install_folder/resources].
