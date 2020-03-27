---
description: Image Serving är en enkel preprocessor för begäranden som baseras på regler för matchning och ersättning av reguljära uttryck.
seo-description: Image Serving är en enkel preprocessor för begäranden som baseras på regler för matchning och ersättning av reguljära uttryck.
seo-title: Förbehandling av begäran
solution: Experience Manager
title: Förbehandling av begäran
topic: Scene7 Image Serving - Image Rendering API
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Förbehandling av begäran{#request-preprocessing}

Image Serving är en enkel preprocessor för begäranden som baseras på regler för matchning och ersättning av reguljära uttryck.

Regelsamlingar (regeluppsättningar) kan bifogas till varje bildkatalog, inklusive standardkatalogen. Regler anges med XML-formaterade filer.

Regler för förbehandling av begäranden kan ändra sökvägen och frågedelarna av begäranden innan de bearbetas av plattformsserverns parser, inklusive att ändra sökvägen, lägga till kommandon, ändra kommandovärden och använda mallar eller makron. Regler kan också användas för att konfigurera och åsidosätta vissa säkerhetsfunktioner som normalt bara styrs med katalogattribut, till exempel begärandeförfalskning, vattenmärkning och begränsning av HTTP-tjänsten till specifika IP-adresser för klienter.

Regler för förbehandling av begäranden är lämpliga för ett antal olika program, varav vissa anges nedan:

* Implementera en *virtuell sökvägsmekanism* som tillåter ommappning av sökvägen till fil-, FTP- och HTTP-sökvägar.
* Selektivt använda säkerhetsfunktioner, som vattenstämplar, filtrerade efter bildnamn eller sökväg.
* Utelämnar vattenstämplar eller andra säkerhetsfunktioner när servern hämtas från specifika IP-adresser.
* Tvingar kommandon, t.ex. `defaultImage=`, att tillämpas på alla förfrågningar eller förfrågningar som har ett visst mönster i URL-sökvägen eller frågesträngarna.
* Tillåt inte användning av CPU-intensiva kommandon för att förhindra servermissbruk.
* Tillåter att källbilder finns på HTTP- eller FTP-servrar samtidigt som de anges på sökvägen i stället för med `src=`.
* Styr inställningarna för bildkvalitet (till exempel JPEG-kvalitet eller skärpa) beroende på sökvägen eller bildnamnet som efterfrågas.

Detaljerad information om hur du skapar, använder och hanterar regeluppsättningar finns i Referenshandbok för [regeluppsättningar](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Se även {#see-also}

[Regeluppsättningsreferens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attribut::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
