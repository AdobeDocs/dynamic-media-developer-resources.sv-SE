---
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
seo-description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
seo-title: Teknikstöd
solution: Experience Manager
title: Teknikstöd
uuid: 9de323c9-d383-41e9-ae44-06600f44a85e
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Textbunden zoom,Tillgänglighet
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---


# Stöd för hjälpfunktioner{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har rollattributen `region` och `aria-label` inställda som standard på visningsprogrammets namn. Du kan styra etiketten med lokaliseringssymbolen `Container.LABEL`.

Huvudvyn har rollen `application`. En kort beskrivning av huvudvyn finns i `aria-roledescription`, med det värde som definieras av lokaliseringssymbolen `ROLE_DESCRIPTION` för motsvarande huvudvykomponent. Navigeringstips för tangentbordsanvändare tillhandahålls med `aria-describedby`, texten för användartipset kommer från lokaliseringssymbolen `USAGE_HINT`. Om en resurs har en etikett definierad i fältet UserData ställs attributet `aria-label` in med värdet för den etiketten.

Komponenter som visar färgrutor har rollen `listbox` med attributet `aria-label` inställt på värdet för `LABEL`-lokaliseringssymbolen för den komponenten. Enskilda färgrutor har rollen `option` med attributen `aria-setsize` och `aria-posinset` som beskriver färgrutans position i uppsättningen. Om du väljer en färgruta får den attributet `aria-selected` inställt på `true`.
