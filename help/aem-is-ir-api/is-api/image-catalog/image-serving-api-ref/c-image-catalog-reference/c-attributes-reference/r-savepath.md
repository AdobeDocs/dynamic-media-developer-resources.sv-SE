---
description: Rotsökväg för saveToFile=. Relativ sökväg för rotmappen som bilder som skapats med req=saveToFile ska skrivas till.
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

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
