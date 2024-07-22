---
title: Resursrotmappar (ir.resourceRootPaths)
description: En lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# Resursrotmappar (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

En lista med sökvägar, avgränsade med semikolon, fungerar som rötter för alla datafiler med relativa filsökvägar.

Det kan antingen vara absoluta sökvägar eller sökvägar i förhållande till *[!DNL install_folder]*. När flera sökvägar har angetts försöker servern varje rot i den angivna ordningen tills filen hittas. Standardvärdet är [!DNL ./resources] för standardrotsökvägen [!DNL install_folder/resources].
