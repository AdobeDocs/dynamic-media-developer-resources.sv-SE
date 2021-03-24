---
description: 'Bilden som returneras till klienten som svar på en req=tmb-begäran härleds från den sammansatta bilden genom att ta hänsyn till följande värden: wid=, hei=, attribute DefaultThumbPix och attribute MaxPix.'
solution: Experience Manager
title: Visa omformning för miniatyrbilder
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Visa omformning för miniatyrbilder{#view-transform-for-thumbnails}

Bilden som returneras till klienten som svar på en req=tmb-begäran härleds från den sammansatta bilden genom att ta hänsyn till följande värden: wid=, hei=, attribute::DefaultThumbPix och attribute::MaxPix.

1. **Beräkna vyrektangeln**  - Använd  `wid=` eller breddvärdet  `attribute::DefaultThumbPix` för vyrektangelns bredd. Använd `hei=` eller höjdvärdet `attribute::DefaultThumbPix` som höjd. Vyrektangeln måste anges fullständigt i det här steget. (Observera att vyrektangeln är densamma som lagret 0 rect, om inget `size=`är angivet för lager 0).
1. **Skala det sammansatta**  - Om  `catalog::ThumbType=Crop`så skalas det sammansatta fotot till minsta möjliga bild medan hela vyrektangeln fortfarande fylls. extra bilddata beskärs. Om `catalog::ThumbType= Fit` skalas den sammansatta bilden till den största möjliga bilden medan hela den sammansatta bilden fortfarande passas in i vyrektangeln. Om `catalog::ThumbType=Texture` ändras inte den sammansatta skalan alls för att bevara upplösningen som anges i `catalog::ThumbRes`.
1. **Fyllning och beskärning**  - vyrektangeln fylls med  `bgc=` färgen (eller, om inget anges, med  `attribute::ThumbBkgColor`). Den skalade sammansatta bilden justeras mot vyrektangeln med hjälp av attributet: `ThumbHorizAlign` och attribut: `ThumbVertAlign`. Den skalade sammansatta bilden sammanfogas sedan med den fyllda vyrektangeln utan ytterligare skalförändring. De områden i den sammansatta bilden som sträcker sig utanför vyrektangeln beskärs.

