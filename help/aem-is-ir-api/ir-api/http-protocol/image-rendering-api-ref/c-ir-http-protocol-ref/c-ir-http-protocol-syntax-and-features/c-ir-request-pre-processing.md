---
description: Bildåtergivning ger en enkel förprocessor för begäranden baserad på regler för matchning och ersättning av reguljära uttryck.
seo-description: Bildåtergivning ger en enkel förprocessor för begäranden baserad på regler för matchning och ersättning av reguljära uttryck.
seo-title: Förbehandling av begäran *
solution: Experience Manager
title: Förbehandling av begäran *
topic: Scene7 Image Serving - Image Rendering API
uuid: ef69ea23-753c-40c8-9edd-eab9c8820c98
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Förbehandling av begäran *{#request-pre-processing}

Bildåtergivning ger en enkel förprocessor för begäranden baserad på regler för matchning och ersättning av reguljära uttryck.

Regelsamlingar (regeluppsättningar) kan bifogas till varje materialkatalog, inklusive standardkatalogen. Regler anges med XML-formaterade filer.

Regler för förbehandling av begäranden kan ändra sökvägen och skicka frågor till delar av begäranden innan de bearbetas av tolken för bildåtergivning, inklusive ändra sökvägen, lägga till kommandon, ändra kommandovärden och använda mallar eller makron. Regler kan också användas för att konfigurera och åsidosätta vissa funktioner som normalt bara styrs med katalogattribut, som att ange standardstorlek för svarsbilder eller begränsa HTTP-tjänsten till specifika IP-adresser för klienter.

Förbearbetningsregler för begäranden passar ett antal olika program, varav vissa anges nedan:

* Implementera en *virtuell sökvägsmekanism* som tillåter ommappning av sökvägen till fil-, FTP- och HTTP-sökvägar.
* Tillåt inte användning av processorintensiva kommandon för att förhindra servermissbruk.
* Styr inställningarna för bildkvalitet (till exempel JPEG-kvalitet eller skärpa) beroende på sökvägen eller bildnamnet som efterfrågas.

Detaljerad information om hur du skapar, använder och hanterar regeluppsättningar finns i Referens för regeluppsättning.

Se även Referens för regeluppsättning, attribut::RuleSetFile
