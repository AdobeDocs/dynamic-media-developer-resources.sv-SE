---
description: Webbdomäner för Flash-program. Adobe Flash-program kan kräva åtkomst till egenskaperna för bilder som levereras i swf-format. SWF-filen måste bevilja åtkomst uttryckligen genom att registrera namnet på de programdomäner som den litar på.
seo-description: Webbdomäner för Flash-program. Adobe Flash-program kan kräva åtkomst till egenskaperna för bilder som levereras i swf-format. SWF-filen måste bevilja åtkomst uttryckligen genom att registrera namnet på de programdomäner som den litar på.
seo-title: Betrodda domäner *
solution: Experience Manager
title: Betrodda domäner *
topic: Scene7 Image Serving - Image Rendering API
uuid: c50180b1-9af7-45f1-878f-59f41f9958ae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Betrodda domäner *{#trusteddomains}

Webbdomäner för Flash-program. Adobe Flash-program kan kräva åtkomst till egenskaperna för bilder som levereras i swf-format. SWF-filen måste bevilja åtkomst uttryckligen genom att registrera namnet på de programdomäner som den litar på.

## Egenskaper {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Sträng som innehåller en kommaavgränsad lista med webbdomännamn. Om det är tomt måste program hanteras från samma domän som bildåtergivning för att kunna komma åt egenskaper för bilder i [!DNL swf]formaterade svar.

## Standard {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Ärvs från `default::TrustedDomains` om det inte finns någon.

## Se även {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribut::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
