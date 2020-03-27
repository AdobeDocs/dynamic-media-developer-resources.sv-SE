---
description: Lager sätts samman i den ordning som anges av kommandot layer=, där lager med högre nummer döljer lager med lägre nummer.
seo-description: Lager sätts samman i den ordning som anges av kommandot layer=, där lager med högre nummer döljer lager med lägre nummer.
seo-title: Den sammansatta arbetsytan
solution: Experience Manager
title: Den sammansatta arbetsytan
topic: Scene7 Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Den sammansatta arbetsytan{#the-compositing-canvas}

Lager sätts samman i den ordning som anges av kommandot layer=, där lager med högre nummer döljer lager med lägre nummer.

Lager 0 utgör bakgrundslagret, som alltid krävs och som definierar den sammansatta bildens storlek. Alla lagertyper tillåts för lager 0. Storleken på lager 0 måste definieras, antingen explicit med `size=` eller implicit, baserat på innehållsbilden eller texten. De områden i andra lager som ligger utanför lagrets område 0 tas inte med i utdatabilden.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>När alla lager har förenklats konverteras den sammansatta bilden till den slutliga svarsbilden enligt [visningskommandona och attributen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).

