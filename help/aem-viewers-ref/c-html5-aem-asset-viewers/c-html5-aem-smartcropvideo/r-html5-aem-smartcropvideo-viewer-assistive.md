---
title: Teknikstöd
description: Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
exl-id: b2bfd93b-707e-4a03-a14e-14ec23328fdd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Teknikstöd{#assistive-technology-support}

Alla visningsprogramkomponenter har stöd för ARIA-roller (Accessible Rich Internet Applications) och -attribut för att förbättra integrationen med hjälpmedelstekniker som skärmläsare.

Visningsprogramelementet på den översta nivån har en roll `region` och `aria-label` som standard anges visningsprogrammets namn. Du kan styra etiketten med `Container.LABEL` lokaliseringssymbol.

Knappar har rollen `button` och beskrivande text med `aria-label` -attribut. Värdet för `aria-label` -attributet fylls i från värdet för knappens lokaliseringssymbol. När en knapp är inaktiverad `aria-disabled` -attributet anges därefter.

Slider-komponenter har rollen `slider` med attribut `aria-valuenow`, `aria-valuemin`och `aria-valuemax` för att beskriva den aktuella skjutreglagepositionen.

Listrutor aktiveras av knappar med ytterligare `aria-haspopup` attribut inställt på `true` och `aria-controls` attribut som refererar till det faktiska nedrullningsbara panelelementet. Den nedrullningsbara panelen har rollen `menu` med delelement som har rollen `menuitem`. Varje menyalternativ har `aria-label` angivet attribut.

Modala dialogrutor har rollen `dialog`. Dialogrutans rubrikelement refereras av `aria-labelledby` -attribut.
