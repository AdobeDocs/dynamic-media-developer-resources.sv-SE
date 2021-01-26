---
description: Bildåtergivning tillämpar en storleksbegränsning på två megapixlar för vinjetter som inte är pyramidbaserade.
seo-description: Bildåtergivning tillämpar en storleksbegränsning på två megapixlar för vinjetter som inte är pyramidbaserade.
seo-title: Storleksbegränsning för vinjett
solution: Experience Manager
title: Storleksbegränsning för vinjett
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# Storleksbegränsning för vinjett{#vignette-size-limitation}

Bildåtergivning tillämpar en storleksbegränsning på två megapixlar för vinjetter som inte är pyramidbaserade.

Ändra värdet för `IrMaxNonPyrVignetteSize` i [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] om ditt program kräver stöd för icke-pyramidvinjettering med ett bildområde (bredd x höjd) som är större än denna gräns.

>[!NOTE]
>
>`attribute::MaxPix` och  `IS::MaxMessageSize` kan också behöva justeras för att tillåta ovanligt stora svarsbilder. Mer information finns i dokumentationen om bildservning.

