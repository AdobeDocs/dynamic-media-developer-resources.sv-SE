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

Bilden som returneras till klienten som svar på en `req=img` begäran härleds från den sammansatta bilden genom att ta hänsyn till följande värden: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`och den sammansatta bildens storlek.

If `wid=` och `hei=` anges, och `scl=` inte är det, den sammansatta bilden skalas så att den passar helt i vyrektangeln som definieras av `wid=` och `hei=`. Om vyrektangelns proportioner skiljer sig från den sammansatta bildens, justeras den skalade sammansatta bilden inom vyrektangeln med hjälp av `align=` värdet, om det anges, eller om det centreras på annat sätt. Alla blanksteg som inte täcks av bilddata fylls med `bgc=` eller, om inget anges, med `attribute::BkgColor`.

If `scl=` anges skalas den sammansatta bilden med den skalningsfaktorn. If `wid=` och/eller `hei=` anges också, beskärs den skalförändrade bilden till `wid=` och/eller `hei=` eller extra utrymme läggs till efter behov. `align=` anger var bilden beskärs eller när extra utrymme läggs till, och eventuellt extra utrymme fylls med `bgc=` eller `attribute::BkgColor`.

Om ingen `wid=`, `hei=` eller `scl=` anges, och om den sammansatta bildens bredd eller höjd överstiger `attribute::DefaultPix`, skalas den sammansatta bilden så att den inte överskrider `attribute::DefaultPix`. I annat fall används den sammansatta bilden utan skalförändring.

Om du vill försäkra dig om att visningsbilden returneras utan ytterligare skalning anger du `scl=1`.

If `rgn=` anges beskärs svarsbilden därefter så att den slutliga svarsbildens storlek uppnås. Den här storleken jämförs med `attribute::MaxPix` (om det är definierat) och ett fel genereras om svarsbilden är större i någon dimension.

If `fmt=` anger data utan alfa, och genomskinliga områden i svarsbilden fylls med `bgc=` eller `attribute::BkgColor`.
