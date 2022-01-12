---
title: Teknikstöd
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

# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har en roll `region` och `aria-label` som standard anges visningsprogrammets namn. Du kan styra etiketten med `Container.LABEL` lokaliseringssymbol.

Huvudvyn har en roll `application`. En kort beskrivning av huvudvyn finns i `aria-roledescription`, med det värde som definieras av `ROLE_DESCRIPTION` lokaliseringssymbol för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`, kommer texten för användartipset från `USAGE_HINT` lokaliseringssymbol. Om en resurs har en etikett definierad i fältet UserData, `aria-label` -attributet anges med värdet för den etiketten.

Komponenter som visar färgrutor har rollen `listbox` med `aria-label` attributet inställt på värdet för `LABEL` lokaliseringssymbol för den komponenten. Enskilda färgrutor har rollen `option` med `aria-setsize` och `aria-posinset` attribut som beskriver färgrutans placering i uppsättningen. Om en färgruta är markerad hämtas `aria-selected` attribut inställt på `true`.
