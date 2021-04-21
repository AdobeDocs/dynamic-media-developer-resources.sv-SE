---
description: Standardkatalogen innehåller standardvärden för alla katalogattribut för alla bildkataloger.
solution: Experience Manager
title: Standardkatalog
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# Standardkatalog{#default-catalog}

Standardkatalogen innehåller standardvärden för alla katalogattribut för alla bildkataloger.

Om det inte går att hitta ett visst attribut i en viss bildkatalog använder servern i stället motsvarande värde från standardkatalogen. På samma sätt kan du använda standardkatalogen för att tillhandahålla standardvärden för specifika katalogdataposter (bilder, makrodefinitioner, teckensnitt och ICC-profiler). Om en viss datapost inte kan hittas i en viss bildkatalog försöker servern att hitta den i standardkatalogen i stället. Detta gör att bildkataloger kan vara glesare ifyllda och förenklar hanteringen av globala attribut och data, som delade mallar, makron, teckensnitt osv.

Dessutom innehåller standardkatalogen alla attribut och dataposter (makron, teckensnitt, ICC-profiler, begär förbearbetningsregler) när ingen specifik bildkatalog är inblandad i en åtgärd.

För att plattformsservern ska fungera korrekt måste katalogattributfilen för standardkatalogen ha namnet [!DNL default.ini], måste alltid finnas i katalogmappen och måste vara fullt ifylld med alla nödvändiga attribut, förutom `attribute::RootId` och referenserna till de olika katalogdatafilerna, som alla är valfria.

>[!NOTE]
>
>Alla katalogattributfiler utom [!DNL default.ini] måste innehålla ett unikt `attribute::RootId`-värde. `attribute::RootId` måste  [!DNL default.ini] vara tom.

