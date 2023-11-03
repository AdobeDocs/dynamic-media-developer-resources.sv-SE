---
description: Det här är den primära loggen som håller reda på alla HTTP-begäranden som gjorts till [!DNL Platform Server]. Om Bildåtergivning är aktiverat skrivs dess åtkomstloggdata till samma fil.
solution: Experience Manager
title: Åtkomstlogg
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Åtkomstlogg{#access-log}

Det här är den primära loggen som håller reda på alla HTTP-begäranden som gjorts till [!DNL Platform Server]. Om Bildåtergivning är aktiverat skrivs dess åtkomstloggdata till samma fil.

Åtkomstloggen är konfigurerad i server.xml.

>[!NOTE]
>
>Utöver klienttrafik för Image Serving ( [!DNL /is/image/*]) och bildåtergivning ( [!DNL /ir/render/*]) kan åtkomstloggen innehålla viss intern trafik: åtkomst till [!DNL Platform Server] katalogsystem ( [!DNL /is-catalog/*]), cachedelning och omdirigeringsbegäranden för fel ( [!DNL /is/cache/*]), åtkomst till andra paket som distribueras till [!DNL Platform Server], t.ex. Dynamic Media Viewer ( [!DNL /is-viewers/*]), statisk trafik och förfrågningar om statiskt innehåll från [!DNL Platform Server] (till exempel [!DNL /is-docs/*]).

Förfrågningar med [!DNL /is-catalog] och [!DNL /is/cache] rotsökvägar ska alltid uteslutas vid klienttrafikanalys.
