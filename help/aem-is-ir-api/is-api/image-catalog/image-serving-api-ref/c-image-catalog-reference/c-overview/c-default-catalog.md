---
description: Standardkatalogen innehåller standardvärden för alla katalogattribut för alla bildkataloger.
solution: Experience Manager
title: Standardkatalog
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Standardkatalog{#default-catalog}

Standardkatalogen innehåller standardvärden för alla katalogattribut för alla bildkataloger.

Om det inte går att hitta ett visst attribut i en viss bildkatalog använder servern i stället motsvarande värde från standardkatalogen. På samma sätt kan du använda standardkatalogen för att tillhandahålla standardvärden för specifika katalogdataposter (bilder, makrodefinitioner, teckensnitt och ICC-profiler). Om en viss datapost inte kan hittas i en viss bildkatalog försöker servern att hitta den i standardkatalogen i stället. Detta gör att bildkataloger kan vara glesare ifyllda och förenklar hanteringen av globala attribut och data, som delade mallar, makron, teckensnitt osv.

Dessutom innehåller standardkatalogen alla attribut och dataposter (makron, teckensnitt, ICC-profiler, begär förbearbetningsregler) när ingen specifik bildkatalog är inblandad i en åtgärd.

För att [!DNL Platform Server] ska fungera korrekt måste katalogattributfilen för standardkatalogen ha namnet [!DNL default.ini], alltid finnas i katalogmappen, och den måste vara fullt ifylld med alla nödvändiga attribut, exklusive `attribute::RootId` och referenserna till de olika katalogdatafilerna, som alla är valfria.

>[!NOTE]
>
>Alla katalogattributfiler utom [!DNL default.ini] måste innehålla ett unikt `attribute::RootId`-värde. `attribute::RootId` i [!DNL default.ini] måste vara tom.
