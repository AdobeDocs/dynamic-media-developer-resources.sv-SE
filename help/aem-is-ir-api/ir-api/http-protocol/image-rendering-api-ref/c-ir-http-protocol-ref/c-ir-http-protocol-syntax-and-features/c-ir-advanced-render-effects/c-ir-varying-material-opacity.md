---
description: Variabel opacitet stöds för heltäckande färg och repeterbara texturer som används på överlappande objekt samt för dekorationer och fönsterövertäckningsmaterial.
solution: Experience Manager
title: Varierande materialopacitet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Varierande materialopacitet{#varying-material-opacity}

Variabel opacitet stöds för heltäckande färg och repeterbara texturer som används på överlappande objekt samt för dekorationer och fönsterövertäckningsmaterial.

Du kan ange opacitetsinformation genom att använda en RGB-bild med en alfakanal. Dessutom kan den övergripande opaciteten varieras med kommandot `opacity=` (både för RGB- och RGBA-bilder).

Vägggränser har också stöd för RGBA-bilder, främst för att stödja urklippsgränser.

Filerna [!DNL vnw] som definierar fönsteromslutningar kan innehålla en opacitetskanal, som kombineras av renderaren med alfakanalen för den repeterbara texturen och `opacity=`-värdet för att ge ett fullständigt urval av opacitetseffekter för enkla och genomskinliga fönsterbehandlingar.
