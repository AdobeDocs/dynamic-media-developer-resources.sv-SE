---
description: Bädda in bandata. Anger om Photoshop-banor från källbildfilen för lager 0 ska inkluderas i svarsbilden.
seo-description: Bädda in bandata. Anger om Photoshop-banor från källbildfilen för lager 0 ska inkluderas i svarsbilden.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: 93e63c7c-c091-4bb1-baff-45706fd611ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# pathEmbed{#pathembed}

Bädda in bandata. Anger om Photoshop-banor från källbildfilen för lager 0 ska inkluderas i svarsbilden.

`pathEmbed=0|1`

## Egenskaper {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Begär attribut. Ignoreras om källbilden inte innehåller sökvägsdata. Banans data skalas och roteras på samma sätt som bilddata. Endast sökvägar från källbilden av `layer=0` bearbetas. banor från andra lagerbilder ignoreras.

Ignoreras om utdatabildformatet inte stöder baninbäddning. Se beskrivningen av `fmt=` för en lista över utdatabildformat som stöder baninbäddning.

## Begränsningar {#section-697cddb79a1542bc8457d2f4f59eec69}

Öppna Photoshop-sökvägar (sökvägar som inte bildar stängda slingor) stöds för närvarande inte för inbäddning i svarsbilden.

## Standard {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, utan inbäddning av banor i utdatabilder.

## Se även {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
