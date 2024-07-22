---
description: Ange trimningsmarginal. Anger den trimningsmarginal som är angiven i filen PDF.
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# trimMargin{#trimmargin}

Ange trimningsmarginal. Anger den trimningsmarginal som är angiven i filen PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` i punkter

Som standard är `trimMargin` inställd på den fullständiga storleken för dokumentet som definieras av `viewWidth` och `viewHeight`. Värdena *[!DNL left]*, *[!DNL bottom]* och *[!DNL right]* får standardvärdet *[!DNL top]* om de inte anges.
