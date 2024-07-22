---
description: Visa omformning för bilder
solution: Experience Manager
title: Visa omformning för bilder
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Visa omformning för bilder{#view-transform-for-images}

Bilden som returneras till klienten som svar på en `req=img`-begäran härleds från den sammansatta bilden genom att ta hänsyn till följande värden: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` och den sammansatta bildens storlek.

Om `wid=` och `hei=` anges, och `scl=` inte anges, skalas den sammansatta bilden så att den passar helt i vyrektangeln som definieras av `wid=` och `hei=`. Om vyrektangelns proportioner skiljer sig från den sammansatta bildens, justeras den skalade sammansatta bilden inom vyrektangeln med hjälp av värdet `align=`, om det anges, eller om den i annat fall centreras. Alla blanksteg som inte täcks av bilddata fylls med `bgc=` eller, om de inte anges, med `attribute::BkgColor`.

Om `scl=` anges skalas den sammansatta bilden med den skalningsfaktorn. Om även `wid=` och/eller `hei=` anges beskärs den skalade bilden till `wid=` och/eller `hei=` eller så läggs extra utrymme till efter behov. `align=` anger var bilden beskärs eller ett extra utrymme läggs till, och eventuellt extra utrymme fylls med `bgc=` eller `attribute::BkgColor`.

Om varken `wid=`, `hei=` eller `scl=` anges och om den sammansatta bildens bredd eller höjd överstiger `attribute::DefaultPix`, skalas den sammansatta bilden så att den inte överskrider `attribute::DefaultPix`. I annat fall används den sammansatta bilden utan skalförändring.

Ange `scl=1` för att garantera att visningsbilden returneras utan ytterligare skalning.

Om `rgn=` anges beskärs svarsbilden därefter så att den slutliga svarsbildens storlek uppnås. Den här storleken jämförs med `attribute::MaxPix` (om den är definierad) och ett fel genereras om svarsbilden är större i någon dimension.

Om `fmt=` anger data utan alfa fylls alla genomskinliga områden i svarsbilden med `bgc=` eller `attribute::BkgColor`.
