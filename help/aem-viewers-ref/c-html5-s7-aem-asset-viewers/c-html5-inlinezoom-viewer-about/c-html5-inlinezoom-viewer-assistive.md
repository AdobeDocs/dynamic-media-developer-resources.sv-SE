---
title: Stöd för hjälpmedel
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,User
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Stöd för hjälpmedel{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningselementet på den översta nivån har rollen `region` och attributet `aria-label` inställt som standard på visningsprogrammets namn. Du kan styra etiketten med lokaliseringssymbolen `Container.LABEL`.

Huvudvyn har rollen `application`. En kort beskrivning av huvudvyn tillhandahålls i `aria-roledescription`, med det värde som definieras av `ROLE_DESCRIPTION`-lokaliseringssymbolen för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`. Texten för användartipset kommer från `USAGE_HINT`-lokaliseringssymbolen. Om en resurs har en etikett definierad i fältet UserData ställs attributet `aria-label` in med värdet för den etiketten.

Komponenter som visar färgrutor har rollen `listbox` med attributet `aria-label` inställt på värdet för `LABEL`-lokaliseringssymbolen för den komponenten. Enskilda färgrutor har rollen `option` med attributen `aria-setsize` och `aria-posinset` som beskriver färgrutans position i uppsättningen. Om du väljer en färgruta får den attributet `aria-selected` inställt på `true`.
