---
description: Rotsökväg för saveToFile=. Relativ sökväg för rotmappen som bilder som skapats med req=saveToFile ska skrivas till.
seo-description: Rotsökväg för saveToFile=. Relativ sökväg för rotmappen som bilder som skapats med req=saveToFile ska skrivas till.
seo-title: SavePath
solution: Experience Manager
title: SavePath
topic: Scene7 Image Serving - Image Rendering API
uuid: 02b88e83-7fee-40d4-95ea-daba9a608e8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SavePath{#savepath}

Rotsökväg för saveToFile=. Relativ sökväg för rotmappen som bilder som skapats med req=saveToFile ska skrivas till.

`SavePath` är ett textsträngsvärde.

## Egenskaper {#section-343d1371e966491c92854a8df14c3c50}

Textsträng. Måste vara tom eller en giltig relativ mappsökväg. Kombineras alltid med den absoluta rotsökvägen som konfigurerats med `ImageServer::SaveDirectory`.

## Standard {#section-ae751eea97654f399c6aaee3f3252cbb}

Ärvs från `default::SavePath` om inte definierat. Spara till filer är inaktiverat om det lösta värdet är tomt.

## Se även {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
