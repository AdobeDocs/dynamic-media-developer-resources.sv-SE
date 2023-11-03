---
description: textPs= implementerar en egen kopieringsalgoritm som automatiskt anpassar teckensnittsstorlekarna så att textområdet fylls optimalt med text, vilket minimerar det extra utrymmet längst ned samtidigt som spill undviks.
solution: Experience Manager
title: Kopia
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Kopia{#copy-fitting}

textPs= implementerar en egen kopieringsalgoritm som automatiskt anpassar teckensnittsstorlekarna så att textområdet fylls optimalt med text, vilket minimerar det extra utrymmet längst ned samtidigt som spill undviks.

Textpassning kan aktiveras och kontrolleras gemensamt för hela textlagret, på styckebasis, även för ett enskilt textintervall.

Ange den minsta teckenstorleken med `\fs` och den maximala teckenstorleken med `\copyfit`. Ett valfritt antal intervall tillåts i samma RTF-sträng. Storleken för alla intervall varierar proportionellt, vilket säkerställer att de önskade storleksförhållandena för teckensnitt behålls.

`\copyfit` betraktas som ett teckenformateringskommando och har omfångsregler som `\fs` och `\b`.

Textpassning är inaktiverat genom att ange `\copyfit` med en storlek som är lika med eller mindre än den storlek som anges med `\fs`.

## Begränsa antalet rader {#section-e5aee0f039e04842afc3d6884ed681ac}

Förutom att ange intervall för teckensnittsstorlekar kan funktionen för kopieringspassningsalgoritmen kontrolleras ytterligare med `\copyfitlines` eller `\copyfitmaxlines` -kommandon, som begränsar antalet rader som algoritmen genererar. Båda kommandona accepterar en radräkningsparameter eller 0, för att inte begränsa antalet rader i det kopierade området.

`\copyfitlines` tillåter att text flödar över till ytterligare rader när den inte får plats i det angivna antalet rader. Uttryckliga radbrytningar i det textsegment som ska kopieras respekteras alltid.

`\copyfitmaxlines` trunkerar alltid extra utdatarader som överskrider den angivna gränsen. Det angivna antalet rader överskrids aldrig, även om det finns explicita radbrytningar. I den här versionen av Image Serving får inte mer än N-1 `\line` markörer kan finnas i det kopieringsanpassade textomfånget. Beteendet är odefinierat om den här gränsen överskrids.

## Exempel {#section-f4ddbbfade444560be30a813d90c2c1b}

I följande exempel antas att textens brödtext innehåller variabler med namnet *[!DNL $A$]*, *[!DNL $B$]* och *[!DNL $C$]*.

**Behåll samma proportion mellan teckensnittsstorlekarna i hela intervallet:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* renderas alltid dubbelt så stort som resten av texten. När mycket text anges, *[!DNL $A$]* och *[!DNL $C$]* återges med `\fs10` och *[!DNL $B$]* med `\fs20`. Med lite text *[!DNL $A$]* och *[!DNL $C$]* use `\fs100` och *[!DNL $B$]* `\fs200`.

**Konvertera till en vanlig stor teckenstorlek om bara en liten del av texten ritas:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

I den minsta änden av intervallet *[!DNL $B$]* återges med `\fs20`, dubbelt så stor som *[!DNL $A$]* och *[!DNL $C$]* på `\fs10`. All text ritas på `\fs100` (50 punkter) i den andra änden av intervallet.

**Konvertera till en vanlig liten teckenstorlek om mycket text ska återges:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

All text ritas med \fs10 i den lilla änden av intervallet, medan den är som störst, *[!DNL $A$]* och *[!DNL $C$]* återges med `\fs100` och *[!DNL $B$]* med `\fs200`.

**Inaktivera textpassning för ett inre textintervall:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

Teckenstorleken för *[!DNL $A$]* och *[!DNL $C$]* kan variera mellan 10 och 100, medan *[!DNL $B$]* återges alltid med `\fs50`.

**Begränsa utdata till en enda rad, även om det finns mer lodrätt utrymme, men tillåt att det flödar över till ytterligare rader om för mycket text har angetts för att få plats på en enda rad vid `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Begränsa utdata till en enda rad, även om det finns mer lodrätt utrymme. Om för mycket text har angetts för att få plats på en enda rad vid `\fs10` den trunkeras:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
