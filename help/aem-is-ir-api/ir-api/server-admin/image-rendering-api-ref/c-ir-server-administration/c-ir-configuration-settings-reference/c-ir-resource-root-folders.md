---
description: Lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.
solution: Experience Manager
title: Resursrotmappar (ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Resursrotmappar (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.

Kan antingen vara absoluta sökvägar eller sökvägar i förhållande till *[!DNL install_folder]*. När flera sökvägar har angetts provar servern varje rot i den angivna ordningen tills filen hittas. Standardvärdet är [!DNL ./resources], för standardrotsökvägen [!DNL install_folder/resources].
