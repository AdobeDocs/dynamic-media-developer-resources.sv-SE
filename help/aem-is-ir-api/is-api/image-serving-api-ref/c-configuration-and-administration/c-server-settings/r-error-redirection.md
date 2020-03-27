---
description: Använd de här serverinställningarna för att omdirigera fel.
seo-description: Använd de här serverinställningarna för att omdirigera fel.
seo-title: Felomdirigering
solution: Experience Manager
title: Felomdirigering
topic: Scene7 Image Serving - Image Rendering API
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Felomdirigering{#error-redirection}

Använd de här serverinställningarna för att omdirigera fel.

>[!NOTE]
>
>Rörtecken (|) i nätsökvägen stöds inte för felomdirigering.

## PS::errorRedirect.rootUrl - Omdirigeringsserver {#section-85f22e48d68842a490b0e1191543b558}

Rotwebbadressen ( [!DNL HTTP:// *[!DNL domain]*[: [ *[!DNL port]*]]) för den sekundära Image Serving-distributionen som begäranden som misslyckas lokalt ska omdirigeras till. Omdirigering av fel är inaktiverat (standard) när den här inställningen är tom eller inte definierad.

## PS::errorRedirect.connectTimeout - Timeout för omdirigering av anslutning {#section-3971be8f720d4b32a2cc7860b4085971}

Maximal tid (i msek) som servern väntar på att en anslutning till den sekundära servern ska upprättas innan ett fel returneras till klienten.

## PS::errorRedirect.socketTimeout - Timeout för omdirigeringssvar {#section-69d8579f748d4044bca99dfb64dd523c}

Maximal tid (i msek) väntar servern på att den sekundära servern ska returnera data innan omdirigeringsbegäran avbryts och ett fel returneras till klienten.
