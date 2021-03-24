---
description: Variabel opacitet stöds för heltäckande färg och repeterbara texturer som används på överlappande objekt samt för dekorationer och fönsterövertäckningsmaterial.
solution: Experience Manager
title: Varierande materialopacitet
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# Varierande materialopacitet{#varying-material-opacity}

Variabel opacitet stöds för heltäckande färg och repeterbara texturer som används på överlappande objekt samt för dekorationer och fönsterövertäckningsmaterial.

Du kan ange opacitetsinformation genom att använda en RGB-bild med en alfakanal. Dessutom kan den övergripande opaciteten varieras med kommandot `opacity=` (både för RGB- och RGBA-bilder).

Vägggränser har också stöd för RGBA-bilder, främst för att stödja urklippsgränser.

Filerna [!DNL vnw] som definierar fönsteromslutningar kan innehålla en opacitetskanal, som kombineras av renderaren med alfakanalen för den repeterbara texturen och `opacity=`-värdet för att ge ett fullständigt urval av opacitetseffekter för enkla och genomskinliga fönsterbehandlingar.
