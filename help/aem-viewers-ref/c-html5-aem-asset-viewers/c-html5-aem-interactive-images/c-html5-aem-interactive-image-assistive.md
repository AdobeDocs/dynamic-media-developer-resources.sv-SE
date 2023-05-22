---
title: Teknikstöd
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har en roll `region` och `aria-label` som standard anges visningsprogrammets namn. Du kan styra etiketten med `Container.LABEL` lokaliseringssymbol.

Huvudvyn har en roll `application`. En kort beskrivning av huvudvyn finns i `aria-roledescription`, med det värde som definieras av `ROLE_DESCRIPTION` lokaliseringssymbol för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`, kommer texten för användartipset från `USAGE_HINT` lokaliseringssymbol. Om en resurs har en etikett definierad i fältet UserData, `aria-label` -attributet anges med värdet för den etiketten.

Aktiveringspunkter, regioner och bildscheman har rollen `button` och beskrivande text med `aria-label` -attribut, med värdet för aktiveringspunkten eller bildschemaetiketten. När användaren fokuserar på aktiveringspunkter eller bildscheman visas navigeringstips för tangentbordsanvändare med `aria-describedby`, med texten för användartipset som kommer från `USAGE_HINT` lokaliseringssymbol.
