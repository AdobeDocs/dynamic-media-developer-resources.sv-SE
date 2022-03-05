---
title: Varierande materialopacitet
description: Variabel opacitet stöds för heltäckande färg och repeterbara texturer som används på överlappande objekt samt för dekorationer och fönsterbeläggning.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Varierande materialopacitet{#varying-material-opacity}

Variabel opacitet stöds för heltäckande färg och repeterbara texturer som används på överlappande objekt samt för dekorationer och fönsterbeläggning.

Du kan ange opacitetsinformation genom att använda en RGB-bild med en alfakanal. Dessutom kan den totala opaciteten varieras med `opacity=` (både för RGB och RGBA-bilder).

Vägggränser har också stöd för RGBA-bilder, främst för att stödja urklippsgränser.

The [!DNL vnw] filer som definierar fönstertäckningar kan innehålla en opacitetskanal. Den kombineras av renderaren med alfakanalen för den repeterbara texturen och `opacity=` för att ge ett fullständigt urval av opacitetseffekter för enkla och genomskinliga fönsterbehandlingar.
