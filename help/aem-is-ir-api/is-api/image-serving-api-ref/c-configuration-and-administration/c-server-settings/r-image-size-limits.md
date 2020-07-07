---
description: Använd de här serverinställningarna för att ange bildstorleksbegränsningar.
seo-description: Använd de här serverinställningarna för att ange bildstorleksbegränsningar.
seo-title: Bildstorleksbegränsningar
solution: Experience Manager
title: Bildstorleksbegränsningar
topic: Scene7 Image Serving - Image Rendering API
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# Bildstorleksbegränsningar{#image-size-limits}

Använd de här serverinställningarna för att ange bildstorleksbegränsningar.

## IS::MaxMessageSize - Gräns för svarsstorlek {#section-bd942385d4d144cd904003695d72c85e}

Begränsar storleken på de data som Image Server får skicka till Platform Server. Detta begränsar i själva verket storleken på den kodade/komprimerade svarsbilden som Image Serving kan returnera till klienten via HTTP (Mbytes).

## IS::MaxRenderRgnPixels - Storleksgräns för utdatabild {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Begränsar storleken på de bilder som Image Server kan producera (exklusive bilder som sparats till fil). Heltalsvärde som är större än 0 i miljoner pixlar. Ett fel returneras om en återgivningsåtgärd skulle överskrida storleksgränsen. Standardvärdet är 16.

## IS::MaxSavePixels - storleksgräns för att spara till filer {#section-d1547c4afa88467080ab08356f775e06}

Begränsar storleken på bilder som Image Server skriver till filer med `req=saveToFile` kommandot. Heltalsvärde som är större än 0 i miljoner pixlar. Ett fel returneras om filsparandet skulle överskrida gränsen. Standardvärdet är 100 miljoner pixlar.

## IS::MaxNonDsfSize - storleksgräns för icke-PTIFF-indatabilder {#section-50de28a7158a436393cce5da0d1e4d46}

Den största tillåtna storleken (i pixlar) för bilder som inte är PTIFF-filer som Image Server får öppna. Image Serving returnerar ett fel när ett försök görs att få åtkomst till en bild som inte är PTIFF och som är större än denna gräns.

>[!NOTE]
>
>Om du anger ett för högt värde kan det leda till att Image Server får slut på minne och att fel uppstår, inklusive krascher.

