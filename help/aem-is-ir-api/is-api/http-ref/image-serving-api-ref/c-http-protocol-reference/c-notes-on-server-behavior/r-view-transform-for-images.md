---
description: Visa omformning för bilder
solution: Experience Manager
title: Visa omformning för bilder
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# Visa omformning för bilder{#view-transform-for-images}

Bilden som returneras till klienten som svar på en `req=img`-begäran härleds från den sammansatta bilden genom att ta hänsyn till följande värden: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` och den sammansatta bildens storlek.

Om `wid=` och `hei=` anges, och `scl=` inte anges, skalas den sammansatta bilden så att den passar helt i vyrektangeln som definieras av `wid=` och `hei=`. Om proportionerna för vyrektangeln skiljer sig från proportionerna för den sammansatta bilden justeras den skalade sammansatta bilden inom vyrektangeln med `align=`-värdet, om det anges, eller så centreras den i annat fall. Alla blanksteg som inte täcks av bilddata fylls med `bgc=` eller, om de inte anges, med `attribute::BkgColor`.

Om `scl=` anges skalförändras den sammansatta bilden med den skalfaktorn. Om `wid=` och/eller `hei=` också anges beskärs den skalade bilden till `wid=` och/eller `hei=` eller så läggs extra utrymme till efter behov. `align=` används för att ange var bilden beskärs eller för att lägga till extra utrymme, och eventuellt extra utrymme fylls med  `bgc=` eller  `attribute::BkgColor`.

Om varken `wid=`, `hei=` eller `scl=` har angetts och om den sammansatta bildens bredd eller höjd överstiger `attribute::DefaultPix`, skalas den sammansatta bilden så att den inte överskrider `attribute::DefaultPix`. I annat fall används den sammansatta bilden utan skalförändring.

Om du vill försäkra dig om att visningsbilden returneras utan ytterligare skalning anger du `scl=1`.

Om `rgn=` anges beskärs svarsbilden därefter så att den slutliga svarsbildens storlek uppnås. Storleken jämförs med `attribute::MaxPix` (om den är definierad) och ett fel genereras om svarsbilden är större i någon dimension.

Om `fmt=` anger data utan alfa fylls alla genomskinliga områden i svarsbilden med `bgc=` eller `attribute::BkgColor`.
