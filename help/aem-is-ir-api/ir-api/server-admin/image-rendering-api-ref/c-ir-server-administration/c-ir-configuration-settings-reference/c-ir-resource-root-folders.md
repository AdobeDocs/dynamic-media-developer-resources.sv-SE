---
description: Lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.
solution: Experience Manager
title: Resursrotmappar (ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# Resursrotmappar (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.

Kan antingen vara absoluta sökvägar eller sökvägar i förhållande till *[!DNL install_folder]*. När flera sökvägar har angetts provar servern varje rot i den angivna ordningen tills filen hittas. Standard är [!DNL ./resources], för en standardrotsökväg till [!DNL install_folder/resources].
