---
description: Klientens cachetid till livstid. Antal timmar till utgångsdatum. Används för att hantera klient- och proxyservercachning.
solution: Experience Manager
title: Förfaller
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Förfaller{#expiration}

Klientens cachetid till livstid. Antal timmar till utgångsdatum. Används för att hantera klient- och proxyservercachning.

Se [katalog::Förfallotid](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md) för mer information.

## Egenskaper {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Reellt tal, -2, -1, 0 eller högre. Antal timmar till förfallodatum sedan svarsbilden genererades. Ange 0 om du alltid vill att svarsbilden ska upphöra att gälla omedelbart, vilket i praktiken inaktiverar klientcache-lagring. Ange till -1 för att markera som `never expire`; i det här fallet returnerar servern alltid 403-status som svar på villkorlig `GET` utan att kontrollera om filen faktiskt har ändrats. Ange till -2 om du vill använda standardinställningen från `attribute::Expiration`.

## Standard {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` används om fältet inte finns, om värdet är -2 eller om fältet är tomt.

## Se även {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [katalog::Förfallotid](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
