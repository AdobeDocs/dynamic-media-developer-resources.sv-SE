---
description: 'Bilden som returneras till klienten som svar på en req=tmb-begäran härleds från den sammansatta bilden genom att ta hänsyn till följande värden: wid=, hei=, attribute DefaultThumbPix och attribute MaxPix.'
solution: Experience Manager
title: Visa omformning för miniatyrbilder
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Visa omformning för miniatyrbilder{#view-transform-for-thumbnails}

Bilden som returneras till klienten som svar på en req=tmb-begäran härleds från den sammansatta bilden genom att ta hänsyn till följande värden: wid=, hei=, attribute::DefaultThumbPix och attribute::MaxPix.

1. **Beräkna vyrektangeln** - Användning `wid=` eller breddvärdet för `attribute::DefaultThumbPix` för vyrektangelns bredd. Använd `hei=` eller höjdvärdet för `attribute::DefaultThumbPix` för höjden. Vyrektangeln måste anges fullständigt i det här steget. (Observera att vyrektangeln är densamma som lagret 0 rect, om ingen `size=`anges för lager 0).
1. **Skala den sammansatta bilden** - Om `catalog::ThumbType=Crop`, skalas den sammansatta bilden till minsta möjliga bild medan hela vyrektangeln fortfarande fylls i, extra bilddata beskärs. If `catalog::ThumbType= Fit`så skalas den sammansatta bilden till största möjliga bild medan hela den sammansatta bilden fortfarande passas in i vyrektangeln. If `catalog::ThumbType=Texture`, skalas inte den sammansatta bilden alls för att bevara upplösningen som anges i `catalog::ThumbRes`.
1. **Fylla i och beskära** - Vyrektangeln fylls med `bgc=` färg (eller, om inget anges, med `attribute::ThumbBkgColor`). Den skalade sammansatta bilden justeras mot vyrektangeln med hjälp av attributet: `ThumbHorizAlign` och attribut: `ThumbVertAlign`. Den skalade sammansatta bilden sammanfogas sedan med den fyllda vyrektangeln utan ytterligare skalförändring. De områden i den sammansatta bilden som sträcker sig utanför vyrektangeln beskärs.
