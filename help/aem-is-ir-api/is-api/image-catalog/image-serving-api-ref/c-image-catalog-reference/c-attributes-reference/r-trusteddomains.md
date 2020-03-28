---
description: Webbdomäner för Flash-program. Adobe Flash-program kan kräva åtkomst till egenskaperna för bilder som levereras med fmt=swf eller fmt=swf3.
seo-description: Webbdomäner för Flash-program. Adobe Flash-program kan kräva åtkomst till egenskaperna för bilder som levereras med fmt=swf eller fmt=swf3.
seo-title: Betrodda domäner
solution: Experience Manager
title: Betrodda domäner
topic: Scene7 Image Serving - Image Rendering API
uuid: 1d056d68-b699-413c-897c-8612444735c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Betrodda domäner{#trusteddomains}

Webbdomäner för Flash-program. Adobe Flash-program kan kräva åtkomst till egenskaperna för bilder som levereras med fmt=swf eller fmt=swf3.

SWF-filen måste bevilja åtkomst uttryckligen genom att registrera namnet på de programdomäner som den litar på.

## Egenskaper {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Sträng som innehåller en kommaavgränsad lista med webbdomännamn. Om det är tomt måste program hanteras från samma domän som bildåtergivning för att kunna komma åt egenskaper för bilder i swf-formaterade svar.

## Standard {#section-5c52ed3c7310488380f5a6f9540bf981}

Ärvs från `default::TrustedDomains` om det inte finns någon.

## Se även {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
