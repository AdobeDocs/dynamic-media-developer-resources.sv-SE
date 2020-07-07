---
description: Det här är den primära loggen som håller reda på alla HTTP-begäranden som görs till Platform Server. Om Bildåtergivning är aktiverat skrivs dess åtkomstloggdata till samma fil.
seo-description: Det här är den primära loggen som håller reda på alla HTTP-begäranden som görs till Platform Server. Om Bildåtergivning är aktiverat skrivs dess åtkomstloggdata till samma fil.
seo-title: Åtkomstlogg
solution: Experience Manager
title: Åtkomstlogg
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---


# Åtkomstlogg{#access-log}

Det här är den primära loggen som håller reda på alla HTTP-begäranden som görs till Platform Server. Om Bildåtergivning är aktiverat skrivs dess åtkomstloggdata till samma fil.

Åtkomstloggen är konfigurerad i server.xml.

>[!NOTE]
>
>Utöver klienttrafik för Image Serving ( [!DNL /is/image/*]) och Image Rendering ( [!DNL /ir/render/*]) kan åtkomstloggen innehålla viss intern trafik: behörighet till katalogsystemet för Platform Server ( [!DNL /is-catalog/*]), cachedelning och begäran om omdirigering av fel ( [!DNL /is/cache/*]), åtkomst till andra paket som distribueras till Platform Server, t.ex. Scene7-visningsprogram ( [!DNL /is-viewers/*]), statisk trafik och begäranden om statiskt innehåll som hanteras av Platform Server (t.ex. [!DNL /is-docs/*]).

Begäranden med [!DNL /is-catalog] och [!DNL /is/cache] rotsökvägar ska alltid uteslutas från klienttrafikanalysen.
