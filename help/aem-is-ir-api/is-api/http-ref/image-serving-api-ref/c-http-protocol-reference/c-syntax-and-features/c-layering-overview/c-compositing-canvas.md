---
description: Lager sätts samman i den ordning som anges av kommandot layer=, där lager med högre nummer döljer lager med lägre nummer.
solution: Experience Manager
title: Den sammansatta arbetsytan
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Den sammansatta arbetsytan{#the-compositing-canvas}

Lager sätts samman i den ordning som anges av kommandot layer=, där lager med högre nummer döljer lager med lägre nummer.

Lager 0 utgör bakgrundslagret, som alltid krävs och som definierar den sammansatta bildens storlek. Alla lagertyper tillåts för lager 0. Storleken på lager 0 måste definieras, antingen explicit med `size=` eller implicit, baserat på innehållets bild eller text. De områden i andra lager som ligger utanför lagrets område 0 inkluderas inte i utdatabilden.

>[!NOTE]
>
>När alla lager har förenklats konverteras den sammansatta bilden till den slutliga svarsbilden, enligt vad som anges med [visningskommandona och attributen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
