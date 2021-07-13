---
description: Bildåtergivning tillämpar en storleksbegränsning på två megapixlar för vinjetter som inte är pyramidbaserade.
solution: Experience Manager
title: Storleksbegränsning för vinjett
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# Storleksbegränsning för vinjett{#vignette-size-limitation}

Bildåtergivning tillämpar en storleksbegränsning på två megapixlar för vinjetter som inte är pyramidbaserade.

Ändra värdet för `IrMaxNonPyrVignetteSize` i [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] om ditt program kräver stöd för icke-pyramidvinjettering med ett bildområde (bredd x höjd) som är större än denna gräns.

>[!NOTE]
>
>`attribute::MaxPix` och  `IS::MaxMessageSize` kan också behöva justeras för att tillåta ovanligt stora svarstider för bilder. Mer information finns i dokumentationen om bildservning.
