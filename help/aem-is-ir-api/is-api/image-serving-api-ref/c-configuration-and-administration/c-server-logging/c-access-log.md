---
description: Det här är den primära loggen som håller reda på alla HTTP-begäranden som görs till plattformsservern. Om Bildåtergivning är aktiverat skrivs dess åtkomstloggdata till samma fil.
solution: Experience Manager
title: Åtkomstlogg
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Åtkomstlogg{#access-log}

Det här är den primära loggen som håller reda på alla HTTP-begäranden som görs till plattformsservern. Om Bildåtergivning är aktiverat skrivs dess åtkomstloggdata till samma fil.

Åtkomstloggen är konfigurerad i server.xml.

>[!NOTE]
>
>Utöver klienttrafik för Image Serving ( [!DNL /is/image/*]) och Image Rendering ( [!DNL /ir/render/*]) kan åtkomstloggen innehålla viss intern trafik: åtkomst till katalogsystemet för plattformsservern ( [!DNL /is-catalog/*]), cachedelning och begäran om omdirigering av fel ( [!DNL /is/cache/*]), åtkomst till andra paket som distribueras till plattformsservern, t.ex. Dynamic Media-visningsprogram ( [!DNL /is-viewers/*]), statisk trafik och statiska innehållsbegäranden som hanteras av plattformsservern (t.ex. [!DNL /is-docs/*]).

Begäranden med rotsökvägarna [!DNL /is-catalog] och [!DNL /is/cache] ska alltid uteslutas från klienttrafikanalys.
