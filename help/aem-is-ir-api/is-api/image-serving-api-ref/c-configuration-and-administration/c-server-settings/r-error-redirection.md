---
description: Använd de här serverinställningarna för att omdirigera fel.
solution: Experience Manager
title: Felomdirigering
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Felomdirigering{#error-redirection}

Använd de här serverinställningarna för att omdirigera fel.

>[!NOTE]
>
>Rörtecken (|) i nätsökvägen stöds inte för felomdirigering.

## PS::errorRedirect.rootUrl - Omdirigeringsserver {#section-85f22e48d68842a490b0e1191543b558}

Rot-URL ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]]) för den sekundära Image Serving-distributionen som begäranden som misslyckas lokalt ska omdirigeras till. Omdirigering av fel är inaktiverat (standard) när den här inställningen är tom eller inte definierad.

## PS::errorRedirect.connectTimeout - Timeout för omdirigering {#section-3971be8f720d4b32a2cc7860b4085971}

Maximal tid (i msek) som servern väntar på att en anslutning till den sekundära servern ska upprättas innan ett fel returneras till klienten.

## PS::errorRedirect.socketTimeout - Timeout för omdirigeringssvar {#section-69d8579f748d4044bca99dfb64dd523c}

Maximal tid (i msek) som servern väntar på att den sekundära servern ska returnera data innan omdirigeringsbegäran avbryts och ett fel returneras till klienten.
