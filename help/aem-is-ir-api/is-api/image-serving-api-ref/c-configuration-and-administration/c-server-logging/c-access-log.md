---
description: Det här är den primära loggen som håller reda på alla HTTP-begäranden som görs till plattformsservern. Om Bildåtergivning är aktiverat skrivs dess åtkomstloggdata till samma fil.
seo-description: Det här är den primära loggen som håller reda på alla HTTP-begäranden som görs till plattformsservern. Om Bildåtergivning är aktiverat skrivs dess åtkomstloggdata till samma fil.
seo-title: Åtkomstlogg
solution: Experience Manager
title: Åtkomstlogg
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# Åtkomstlogg{#access-log}

Det här är den primära loggen som håller reda på alla HTTP-begäranden som görs till plattformsservern. Om Bildåtergivning är aktiverat skrivs dess åtkomstloggdata till samma fil.

Åtkomstloggen är konfigurerad i server.xml.

>[!NOTE]
>
>Utöver klienttrafik för Image Serving ( [!DNL /is/image/*]) och Image Rendering ( [!DNL /ir/render/*]) kan åtkomstloggen innehålla viss intern trafik: åtkomst till katalogsystemet för plattformsservern ( [!DNL /is-catalog/*]), cachedelning och begäran om omdirigering av fel ( [!DNL /is/cache/*]), åtkomst till andra paket som distribueras till plattformsservern, t.ex. Dynamic Media-visningsprogram ( [!DNL /is-viewers/*]), statisk trafik och statiska innehållsbegäranden som hanteras av plattformsservern (t.ex. [!DNL /is-docs/*]).

Begäranden med rotsökvägarna [!DNL /is-catalog] och [!DNL /is/cache] ska alltid uteslutas från klienttrafikanalys.
