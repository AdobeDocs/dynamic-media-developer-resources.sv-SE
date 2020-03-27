---
description: 'Bilden som returneras till klienten som svar på en req=tmb-begäran härleds från den sammansatta bilden genom att ta hänsyn till följande värden: wid=, hei=, attribute DefaultThumbPix och attribute MaxPix.'
seo-description: 'Bilden som returneras till klienten som svar på en req=tmb-begäran härleds från den sammansatta bilden genom att ta hänsyn till följande värden: wid=, hei=, attribute DefaultThumbPix och attribute MaxPix.'
seo-title: Visa omformning för miniatyrbilder
solution: Experience Manager
title: Visa omformning för miniatyrbilder
topic: Scene7 Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# Visa omformning för miniatyrbilder{#view-transform-for-thumbnails}

Bilden som returneras till klienten som svar på en req=tmb-begäran härleds från den sammansatta bilden genom att ta hänsyn till följande värden: wid=, hei=, attribute::DefaultThumbPix och attribute::MaxPix.

1. **Beräkna vyrektangeln** - Använd `wid=` eller breddvärdet `attribute::DefaultThumbPix` för vyrektangelns bredd. Använd `hei=` eller höjdvärdet för `attribute::DefaultThumbPix` höjden. Vyrektangeln måste anges fullständigt i det här steget. (Observera att vyrektangeln är densamma som lagret 0 rect, om inget `size=`anges för lagret 0).
1. **Skala den sammansatta** bilden - Om `catalog::ThumbType=Crop`så skalas den sammansatta bilden till minsta möjliga bild medan hela vyrektangeln fortfarande fylls. extra bilddata beskärs. Om du `catalog::ThumbType= Fit`gör det skalas den sammansatta bilden till största möjliga bild samtidigt som hela den sammansatta bilden fortfarande passas in i vyrektangeln. Om `catalog::ThumbType=Texture`det inte finns någon skalning alls för den sammansatta bilden för att bevara upplösningen som anges i `catalog::ThumbRes`.
1. **Fyllning och beskärning** - vyrektangeln fylls med `bgc=` färgen (eller, om inget anges, med `attribute::ThumbBkgColor`). Den skalade sammansatta bilden justeras mot vyrektangeln med hjälp av attributet: `ThumbHorizAlign` och attribut: `ThumbVertAlign`. Den skalade sammansatta bilden sammanfogas sedan med den fyllda vyrektangeln utan ytterligare skalförändring. De områden i den sammansatta bilden som sträcker sig utanför vyrektangeln beskärs.

