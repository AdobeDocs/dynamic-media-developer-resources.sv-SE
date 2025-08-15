---
description: Det här är den primära loggen som håller reda på alla HTTP-begäranden som gjorts till  [!DNL Platform Server]. Om Bildåtergivning är aktiverat skrivs dess åtkomstloggdata till samma fil.
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
>Utöver klienttrafik för Image Serving ( [!DNL /is/image/*]) och Image Rendering ( [!DNL /ir/render/*]) kan åtkomstloggen innehålla viss intern trafik: åtkomst till [!DNL Platform Server]-katalogsystemet ( [!DNL /is-catalog/*]), cachedelning och begäran om felomdirigering ( [!DNL /is/cache/*]), åtkomst till andra paket som distribuerats till [!DNL Platform Server], till exempel Dynamic Media Viewer ( [!DNL /is-viewers/*]), statisk trafik och begäranden om statiskt innehåll från [!DNL Platform Server] (till exempel [!DNL /is-docs/*]).

Begäranden med [!DNL /is-catalog]- och [!DNL /is/cache]-rotsökvägar ska alltid exkluderas från alla klienttrafikanalyser.
