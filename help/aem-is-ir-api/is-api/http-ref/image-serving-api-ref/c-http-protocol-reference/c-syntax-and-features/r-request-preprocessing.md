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

Regler för förbehandling av begäranden kan ändra sökvägen och frågedelarna av begäranden innan de bearbetas av parsern för [!DNL Platform Server], bland annat ändra sökvägen, lägga till kommandon, ändra kommandovärden och använda mallar eller makron. Regler kan också användas för att konfigurera och åsidosätta vissa säkerhetsfunktioner som normalt bara styrs med katalogattribut, till exempel begärandeförfalskning, vattenmärkning, samt för att begränsa HTTP-tjänsten till specifika IP-adresser för klienter.

Regler för förbehandling av begäranden är lämpliga för ett antal olika program, varav vissa anges nedan:

* Implementera en *virtuell sökvägsmekanism* som tillåter ommappning av sökvägen till fil-, FTP- och HTTP-sökvägar.
* Selektivt använda säkerhetsfunktioner, som vattenstämplar, filtrerade efter bildnamn eller sökväg.
* Utelämnar vattenstämplar eller andra säkerhetsfunktioner när servern hämtas från specifika IP-adresser.
* Tillämpning av kommandon, till exempel `defaultImage=`, på alla förfrågningar eller förfrågningar som har ett visst mönster i URL-sökvägen eller frågesträngarna.
* Tillåt inte användning av CPU-intensiva kommandon för att förhindra servermissbruk.
* Tillåter att källbilder hittas på HTTP- eller FTP-servrar samtidigt som de anges på sökvägen för begäran i stället för med `src=`.
* Styr inställningarna för bildkvalitet (t.ex. JPEG-kvalitet eller skärpa) beroende på sökvägen eller bildnamnet.

Detaljerad information om hur du skapar, använder och hanterar regeluppsättningar finns i [Referens för regeluppsättning](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Se även {#see-also}

[Regeluppsättningsreferens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attribut::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
