---
description: Ange mediemarginal. Anger den mediemarginal som anges i PDF-filen.
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

Ange mediemarginal. Anger den mediemarginal som anges i PDF-filen.

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` i punkter

Som standard är `mediaMargin` inställd på den fullständiga storleken för dokumentet som definieras av `viewWidth` och `viewHeight`. Värdena *[!DNL left]*, *[!DNL bottom]* och *[!DNL right]* får standardvärdet *[!DNL top]* om de inte anges.
