---
description: Bädda in XMP metadata. Anger om XMP metadata ska inkluderas i svarsbilden.
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# xmpEmbed{#xmpembed}

Bädda in XMP metadata. Anger om XMP metadata ska inkluderas i svarsbilden.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP data skickas från källbilden till svarsbilden utan ändring. Detta kan leda till att felaktiga data bäddas in i svarsbilden.

## Egenskaper {#section-27024c4272f44d9a8c264a0629193af2}

Begär attribut. Ignoreras om källbilden inte innehåller XMP data. Endast XMP data från källbilden av `layer=0` bearbetas. XMP data från andra lagerbilder ignoreras.

Ignoreras om utdatabildformatet inte stöder XMP inbäddning. Se beskrivningen av `fmt=` för en lista över de utdatabildformat som stöder XMP.

## Standard {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, utan inbäddning av banor i utdatabilder.

## Se även {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
