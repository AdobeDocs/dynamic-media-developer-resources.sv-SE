---
description: 'Bilden som returneras till klienten som svar på en req=tmb-begäran härleds från den sammansatta bilden genom att beakta följande värden: wid=, hei=, attribute DefaultThumbPix och attribute MaxPix.'
solution: Experience Manager
title: Visa omformning för miniatyrbilder
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Visa omformning för miniatyrbilder{#view-transform-for-thumbnails}

Bilden som returneras till klienten som svar på en req=tmb-begäran härleds från den sammansatta bilden genom att ta hänsyn till följande värden: wid=, hei=, attribute::DefaultThumbPix och attribute::MaxPix.

1. **Beräkna vyrektangeln** - Använd `wid=` eller breddvärdet `attribute::DefaultThumbPix` för vyrektangelns bredd. Använd `hei=` eller höjdvärdet `attribute::DefaultThumbPix` för höjden. Vyrektangeln måste anges fullständigt i det här steget. (Observera att vyrektangeln är densamma som lagret 0 rect, om ingen `size=` har angetts för lager 0).
1. **Skala det sammansatta** - Om `catalog::ThumbType=Crop` ändras den sammansatta bilden till minsta möjliga bild medan hela vyrektangeln fylls i. Extra bilddata beskärs. Om `catalog::ThumbType= Fit` skalas den sammansatta bilden till den största möjliga bilden medan hela den sammansatta bilden fortfarande passas in i vyrektangeln. Om `catalog::ThumbType=Texture` skalas inte den sammansatta bilden alls för att bevara upplösningen som anges i `catalog::ThumbRes`.
1. **Fyllning och beskärning** - vyrektangeln fylls med färgen `bgc=` (eller, om den inte anges, med `attribute::ThumbBkgColor`). Den skalade sammansatta bilden justeras mot vyrektangeln med attributet: `ThumbHorizAlign` och attributet: `ThumbVertAlign`. Den skalade sammansatta bilden sammanfogas sedan med den fyllda vyrektangeln utan ytterligare skalförändring. De områden i den sammansatta bilden som sträcker sig utanför vyrektangeln beskärs.
