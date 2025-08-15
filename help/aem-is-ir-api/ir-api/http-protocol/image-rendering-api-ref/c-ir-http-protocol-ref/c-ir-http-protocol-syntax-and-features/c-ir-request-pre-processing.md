---
title: Förbehandling av begäran
description: Bildåtergivning ger en enkel förprocessor för begäranden baserad på regler för matchning och ersättning av reguljära uttryck.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 20f4922402bd31c71ae650a01597b574220809fa
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Förbehandling av begäran{#request-pre-processing}

Bildåtergivning ger en enkel förprocessor för begäranden baserad på regler för matchning och ersättning av reguljära uttryck.

Regelsamlingar (regeluppsättningar) kan bifogas till varje materialkatalog, inklusive standardkatalogen. Regler anges med XML-formaterade filer.

Regler för förbehandling av begäranden kan ändra sökvägen och frågedelarna av begäranden innan de bearbetas av tolken för bildåtergivning. Det här prefixet inkluderar att ändra banan, lägga till kommandon, ändra kommandovärden och använda mallar eller makron. Regler kan också användas för att konfigurera och åsidosätta vissa funktioner som normalt bara styrs med katalogattribut, som att ange standardstorlek för svarsbilder eller begränsa HTTP-tjänsten till specifika IP-adresser för klienter.

Regler för förbehandling av begäranden är lämpliga för olika program, varav vissa anges nedan:

* Implementera en *virtuell sökvägsmekanism* som tillåter ommappning av sökvägen till fil-, FTP- och HTTP-sökvägar.
* Tillåt inte användning av CPU-intensiva kommandon för att förhindra servermissbruk.
* Styr inställningarna för bildkvalitet (t.ex. JPEG-kvalitet eller skärpa) beroende på sökvägen eller bildnamnet.

Detaljerad information om hur du skapar, använder och hanterar regeluppsättningar finns i Referens för regeluppsättning.

Se även Referens för regeluppsättning, attribut::RuleSetFile
