---
description: Bildåtergivning ger en enkel förprocessor för begäranden baserad på regler för matchning och ersättning av reguljära uttryck.
solution: Experience Manager
title: Förbehandling av begäran *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# Förbehandling av begäran *{#request-pre-processing}

Bildåtergivning ger en enkel förprocessor för begäranden baserad på regler för matchning och ersättning av reguljära uttryck.

Regelsamlingar (regeluppsättningar) kan bifogas till varje materialkatalog, inklusive standardkatalogen. Regler anges med XML-formaterade filer.

Regler för förbehandling av begäranden kan ändra sökvägen och skicka frågor till delar av begäranden innan de bearbetas av tolken för bildåtergivning, inklusive ändra sökvägen, lägga till kommandon, ändra kommandovärden och använda mallar eller makron. Regler kan också användas för att konfigurera och åsidosätta vissa funktioner som normalt bara styrs med katalogattribut, som att ange standardstorlek för svarsbilder eller begränsa HTTP-tjänsten till specifika IP-adresser för klienter.

Förbearbetningsregler för begäranden passar ett antal olika program, varav vissa anges nedan:

* Implementera en *virtuell sökväg*-mekanism som tillåter ommappning av sökvägen till fil-, FTP- och HTTP-sökvägar.
* Tillåt inte användning av processorintensiva kommandon för att förhindra servermissbruk.
* Styr inställningarna för bildkvalitet (till exempel JPEG-kvalitet eller skärpa) beroende på sökvägen eller bildnamnet som efterfrågas.

Detaljerad information om hur du skapar, använder och hanterar regeluppsättningar finns i Referens för regeluppsättning.

Se även Referens för regeluppsättning, attribut::RuleSetFile
