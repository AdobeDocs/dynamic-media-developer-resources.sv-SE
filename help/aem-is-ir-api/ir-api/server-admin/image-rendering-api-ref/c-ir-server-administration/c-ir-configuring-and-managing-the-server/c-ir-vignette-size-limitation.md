---
description: Bildåtergivning tillämpar en storleksbegränsning på två megapixlar för vinjetter som inte är pyramidbaserade.
solution: Experience Manager
title: Storleksbegränsning för vinjett
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# Storleksbegränsning för vinjett{#vignette-size-limitation}

Bildåtergivning tillämpar en storleksbegränsning på två megapixlar för vinjetter som inte är pyramidbaserade.

Ändra värdet för `IrMaxNonPyrVignetteSize` i [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] om ditt program kräver stöd för vinjetter som inte är pyramidbaserade och där bildområdet (bredd x höjd) är större än denna gräns.

>[!NOTE]
>
>`attribute::MaxPix` och `IS::MaxMessageSize` kan också behöva justeras för att tillåta ovanligt stora svarstider för bilder. Mer information finns i dokumentationen om bildservning.
