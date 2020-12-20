---
description: Klientens cachetid till livstid. Antal timmar till utgångsdatum. Används för att hantera klient- och proxyservercachning.
seo-description: Klientens cachetid till livstid. Antal timmar till utgångsdatum. Används för att hantera klient- och proxyservercachning.
seo-title: Förfaller
solution: Experience Manager
title: Förfaller
topic: Scene7 Image Serving - Image Rendering API
uuid: 6dbd7d43-727c-42fc-8953-dba112209a45
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---


# Förfallodatum{#expiration}

Klientens cachetid till livstid. Antal timmar till utgångsdatum. Används för att hantera klient- och proxyservercachning.

Servern beräknar förfallotid/datum för NTTP-svarsdata genom att lägga till det här värdet till tid/datum för överföringen.

Webbläsare hanterar cacheminnen med hjälp av filernas förfallotider. Innan webbläsaren skickar en begäran till servern kontrollerar den om filen redan har laddats ned. Om så är fallet, och om filen ännu inte har gått ut, skickar webbläsaren en villkorlig GET-begäran (till exempel med rubriken If-Modified-Since HTTP-begäran) i stället för en vanlig GET-begäran. Servern kan svara med statusen 304 och inte skicka bilden. Webbläsaren läser då bara in filen från cachen. Detta kan avsevärt öka den övergripande prestandan för data som används ofta.

Servern ställer in rubriken för utgående HTTP-svar på aktuellt datum/tid plus det minsta av vinjettering::Förfallotid och alla kataloger::Förfallovärden för vinjetteringen och allt material som ingår i återgivningsåtgärden.

Förfallodatumet anges i första hand för bildsvarningar. Vissa typer av svar kommer alltid att markeras för omedelbar förfallotid (eller taggas som icke-cacheable), inklusive alla felsvar eller egenskapssvar.

## Egenskaper {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Reellt tal, -2, -1, 0 eller högre. Antal timmar till förfallodatum sedan svarsbilden genererades. Ange 0 om du alltid vill att svarsbilden ska upphöra att gälla omedelbart, vilket i praktiken inaktiverar klientcache-lagring. Ange -1 för att markera som `never expire`. I det här fallet returnerar servern alltid 304-status (inte ändrad) som svar på villkorliga `GET`-begäranden utan att kontrollera om filen faktiskt har ändrats. Ange -2 om du vill använda standardvärdet som anges av `attribute::Expiration`.

## Standard {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` används om fältet inte finns, om värdet är -2 eller om fältet är tomt.

## Se även {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
