---
description: Klientens cachetid till livstid. Antal timmar till utgångsdatum. Används för att hantera klient- och proxyservercachning.
seo-description: Klientens cachetid till livstid. Antal timmar till utgångsdatum. Används för att hantera klient- och proxyservercachning.
seo-title: Förfaller
solution: Experience Manager
title: Förfaller
topic: Dynamic Media Image Serving - Image Rendering API
uuid: fa267728-9a36-4705-97d6-d567148fc2d7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# Förfallodatum{#expiration}

Klientens cachetid till livstid. Antal timmar till utgångsdatum. Används för att hantera klient- och proxyservercachning.

Mer information finns i ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)`.

## Egenskaper {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Reellt tal, -2, -1, 0 eller högre. Antal timmar till förfallodatum sedan svarsbilden genererades. Ange 0 om du alltid vill att svarsbilden ska upphöra att gälla omedelbart, vilket i praktiken inaktiverar klientcache-lagring. Ange -1 för att markera som `never expire`; I det här fallet returnerar servern alltid 403-status som svar på villkorliga `GET`-begäranden utan att kontrollera om filen faktiskt har ändrats. Ange -2 om du vill använda standardvärdet som anges av `attribute::Expiration`.

## Standard {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` används om fältet inte finns, om värdet är -2 eller om fältet är tomt.

## Se även {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
