---
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
solution: Experience Manager
title: Teknikstöd
feature: Dynamic Media Classic,visningsprogram,SDK/API,360 VR-video,hjälpmedel
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# Stöd för hjälpfunktioner{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har rollattributen `region` och `aria-label` inställda som standard på visningsprogrammets namn. Du kan styra etiketten med lokaliseringssymbolen `Container.LABEL`.

Knappar har rollen `button` och beskrivande textuppsättning med attributet `aria-label`. Värdet för attributet `aria-label` fylls i från värdet för knappens lokaliseringssymbol. När en knapp är inaktiverad ställs `aria-disabled`-attributet in därefter.

Slider-komponenter har rollen `slider` med attributen `aria-valuenow`, `aria-valuemin` och `aria-valuemax` som beskriver den aktuella skjutreglagepositionen.

Nedrullningsbara listor aktiveras av knappar med ytterligare `aria-haspopup`-attribut inställt på `true` och `aria-controls`-attribut som refererar till det faktiska nedrullningsbara panelelementet. Den nedrullningsbara panelen har rollen `menu` med underelement som har rollen `menuitem`. Varje menyalternativ har det angivna `aria-label`-attributet.

Modala dialogrutor har rollen `dialog`. Dialogrutans rubrikelement refereras av attributet `aria-labelledby`.
