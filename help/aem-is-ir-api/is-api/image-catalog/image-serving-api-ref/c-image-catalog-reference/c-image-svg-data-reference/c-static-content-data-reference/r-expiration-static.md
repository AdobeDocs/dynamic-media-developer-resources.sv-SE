---
title: Förfallotid
description: Används för att hantera klient- och proxyservercachning. Servern beräknar förfallotid/datum för HTTP-svarsdata genom att lägga till det här värdet till tid/datum för överföring.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 064dab12-5f58-4e19-a6b1-fbd20182e3aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Förfallotid{#expiration}

Används för att hantera klient- och proxyservercachning. Servern beräknar förfallotid/datum för HTTP-svarsdata genom att lägga till det här värdet till tid/datum för överföring.

Webbläsare hanterar cacheminnen med hjälp av filernas förfallotider. Innan webbläsaren skickar en begäran till servern kontrollerar den om filen redan har laddats ned. I så fall, och om filen ännu inte har gått ut, skickar webbläsaren en villkorlig GET-begäran (till exempel med fältet Om ändrad-Sedan inställt i begärandehuvudet) i stället för en vanlig GET-begäran. Servern kan svara med statusen 304 och inte skicka bilden. Webbläsaren läser sedan in filen från cachen. Detta kan avsevärt öka den övergripande prestandan för data som används ofta.

Förfallotid används för följande svarstyper:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Vissa typer av svar (till exempel felsvar) är alltid markerade för omedelbar förfallotid (eller taggade som icke-cacheable), medan andra (till exempel egenskaps- eller standardbildsvar) använder speciella förfalloinställningar ( `attribute::NonImgExpiration` och `attribute::DefaultExpiration`).

## Egenskaper {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Reellt tal, -2, -1 eller 0 eller högre. Antal timmar till förfallodatum sedan svarsbilden genererades. Ange 0 om du alltid vill att svarsbilden ska upphöra att gälla omedelbart, vilket i praktiken inaktiverar klientcache-lagring. Ange till -1 för att markera som *`never expire`*. I det här fallet returnerar servern alltid 304-status (inte ändrad) som svar på begäran om villkorlig GET utan att kontrollera om filen faktiskt har ändrats. Ange till -2 om du vill använda standardinställningen från `attribute::Expiration`.

## Standard {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` används om fältet inte finns, om värdet är -2 eller om fältet är tomt.

## Se även {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7), [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d), [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
