---
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
solution: Experience Manager
title: Teknikstöd
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva bilder,Tillgänglighet
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har rollattributen `region` och `aria-label` inställda som standard på visningsprogrammets namn. Du kan styra etiketten med lokaliseringssymbolen `Container.LABEL`.

Huvudvyn har rollen `application`. En kort beskrivning av huvudvyn finns i `aria-roledescription`, med det värde som definieras av lokaliseringssymbolen `ROLE_DESCRIPTION` för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`, texten för användartipset kommer från lokaliseringssymbolen `USAGE_HINT`. Om en resurs har en etikett definierad i fältet UserData ställs attributet `aria-label` in med värdet för den etiketten.

Aktiveringspunkter, regioner och bildscheman har rollen `button` och en beskrivande textuppsättning med attributet `aria-label`, med värdet för aktiveringspunkten eller bildschemats etikett. När användaren fokuserar på aktiveringspunkter eller bildscheman visas navigeringstips för tangentbordsanvändare med `aria-describedby`, där texten för användartipset kommer från lokaliseringssymbolen `USAGE_HINT`.
