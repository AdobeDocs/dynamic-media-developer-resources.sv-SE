---
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
seo-description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
seo-title: Teknikstöd
solution: Experience Manager
title: Teknikstöd
topic: Dynamic media
uuid: 5f6a021f-750c-40e1-be01-86c3750fd25f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har roll `region` och `aria-label` attribut inställt som standard på visningsprogrammets namn. Du kan styra etiketten med `Container.LABEL` lokaliseringssymbolen.

Huvudvyn har en roll `application`. En kort beskrivning av huvudvyn finns i `aria-roledescription`, med det värde som definieras av `ROLE_DESCRIPTION` lokaliseringssymbolen för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`, texten för användartipset kommer från `USAGE_HINT` lokaliseringssymbolen. Om en resurs har en etikett definierad i fältet UserData, ställs attributet in med värdet för den etiketten. `aria-label`

Aktiveringspunkter, regioner och bildscheman har rollen `button` och beskrivande text med `aria-label` attribut, med värdet för aktiveringspunkten eller bildschemats etikett. När användaren fokuserar på aktiveringspunkter eller bildscheman visas navigeringstips för tangentbordsanvändare med `aria-describedby`, där texten för användartipset kommer från `USAGE_HINT` lokaliseringssymbolen.
