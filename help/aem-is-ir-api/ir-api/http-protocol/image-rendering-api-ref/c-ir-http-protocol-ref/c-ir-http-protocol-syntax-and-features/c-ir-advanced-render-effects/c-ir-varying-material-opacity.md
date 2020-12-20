---
description: Variabel opacitet stöds för heltäckande färg och repeterbara texturer som används på överlappande objekt samt för dekorationer och fönsterövertäckningsmaterial.
seo-description: Variabel opacitet stöds för heltäckande färg och repeterbara texturer som används på överlappande objekt samt för dekorationer och fönsterövertäckningsmaterial.
seo-title: Varierande materialopacitet
solution: Experience Manager
title: Varierande materialopacitet
topic: Scene7 Image Serving - Image Rendering API
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Varierande materialopacitet{#varying-material-opacity}

Variabel opacitet stöds för heltäckande färg och repeterbara texturer som används på överlappande objekt samt för dekorationer och fönsterövertäckningsmaterial.

Du kan ange opacitetsinformation genom att använda en RGB-bild med en alfakanal. Dessutom kan den övergripande opaciteten varieras med kommandot `opacity=` (både för RGB- och RGBA-bilder).

Vägggränser har också stöd för RGBA-bilder, främst för att stödja urklippsgränser.

Filerna [!DNL vnw] som definierar fönsteromslutningar kan innehålla en opacitetskanal, som kombineras av renderaren med alfakanalen för den repeterbara texturen och `opacity=`-värdet för att ge ett fullständigt urval av opacitetseffekter för enkla och genomskinliga fönsterbehandlingar.
