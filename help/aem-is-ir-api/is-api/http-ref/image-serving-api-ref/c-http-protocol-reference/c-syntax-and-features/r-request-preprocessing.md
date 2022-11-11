---
description: Image Serving är en enkel preprocessor för begäranden som baseras på regler för matchning och ersättning av reguljära uttryck.
solution: Experience Manager
title: Förbehandling av begäran
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Förbehandling av begäran{#request-preprocessing}

Image Serving är en enkel preprocessor för begäranden som baseras på regler för matchning och ersättning av reguljära uttryck.

Regelsamlingar (regeluppsättningar) kan bifogas till varje bildkatalog, inklusive standardkatalogen. Regler anges med XML-formaterade filer.

Regler för förbehandling av begäranden kan ändra sökväg och frågedelar av begäranden innan de bearbetas av [!DNL Platform Server]parser, som att ändra banan, lägga till kommandon, ändra kommandovärden och använda mallar eller makron. Regler kan också användas för att konfigurera och åsidosätta vissa säkerhetsfunktioner som normalt bara styrs med katalogattribut, till exempel begärandeförfalskning, vattenmärkning och begränsning av HTTP-tjänsten till specifika IP-adresser för klienter.

Regler för förbehandling av begäranden är lämpliga för ett antal olika program, varav vissa anges nedan:

* Implementera en *virtuella sökvägar* som gör det möjligt att mappa om sökvägen till filen, FTP och HTTP-sökvägarna.
* Selektivt använda säkerhetsfunktioner, som vattenstämplar, filtrerade efter bildnamn eller sökväg.
* Utelämnar vattenstämplar eller andra säkerhetsfunktioner när servern hämtas från specifika IP-adresser.
* Tvinga användning av kommandon, som `defaultImage=`, till alla förfrågningar eller förfrågningar som har ett specifikt mönster i URL-sökvägen eller frågesträngarna.
* Tillåt inte användning av CPU-intensiva kommandon för att förhindra servermissbruk.
* Tillåta att källbilder finns på HTTP- eller FTP-servrar samtidigt som de anges på sökvägen i stället för med `src=`.
* Styr inställningarna för bildkvalitet (t.ex. JPEG eller skärpa) beroende på sökvägen eller bildnamnet.

Detaljerad information om hur du skapar, använder och hanterar regeluppsättningar finns i [Regeluppsättningsreferens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Se även {#see-also}

[Regeluppsättningsreferens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attribute::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
