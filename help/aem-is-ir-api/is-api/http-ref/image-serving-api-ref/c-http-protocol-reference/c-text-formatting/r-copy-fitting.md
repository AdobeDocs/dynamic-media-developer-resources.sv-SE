---
description: textPs= implementerar en egen kopieringsalgoritm som automatiskt justerar teckensnittsstorleken för att fylla textområdet optimalt med text, vilket minimerar det extra utrymmet längst ned samtidigt som spill undviks.
seo-description: textPs= implementerar en egen kopieringsalgoritm som automatiskt justerar teckensnittsstorleken för att fylla textområdet optimalt med text, vilket minimerar det extra utrymmet längst ned samtidigt som spill undviks.
seo-title: Kopia
solution: Experience Manager
title: Kopia
uuid: c3ddbf1f-c724-4436-96ff-2c616dfd355d
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 0%

---


# Kopia{#copy-fitting}

textPs= implementerar en egen kopieringsalgoritm som automatiskt justerar teckensnittsstorleken för att fylla textområdet optimalt med text, vilket minimerar det extra utrymmet längst ned samtidigt som spill undviks.

Textpassning kan aktiveras och kontrolleras gemensamt för hela textlagret, på styckebasis, även för ett enskilt textintervall.

Ange den minsta teckenstorleken med `\fs` och den största teckenstorleken med `\copyfit`. Ett valfritt antal intervall tillåts i samma RTF-sträng. Storleken för alla intervall varierar proportionellt, vilket säkerställer att de önskade storleksförhållandena för teckensnitt behålls.

`\copyfit` är ett teckenformateringskommando som har omfångsregler som  `\fs` och  `\b`.

Kopiera-passning inaktiveras genom att ange `\copyfit` med en storlek som är lika med eller mindre än den storlek som anges med `\fs`.

## Begränsa antalet rader {#section-e5aee0f039e04842afc3d6884ed681ac}

Förutom att ange intervall med teckensnittsstorlekar kan funktionen för kopieringspassningsalgoritmen kontrolleras ytterligare med kommandona `\copyfitlines` eller `\copyfitmaxlines`, som begränsar antalet rader som algoritmen ska generera. Båda kommandona accepterar en radräkningsparameter eller 0, för att inte begränsa antalet rader i det kopierade området.

`\copyfitlines` tillåter att text flödar över till ytterligare rader när den inte får plats i det angivna antalet rader. Uttryckliga radbrytningar i det textsegment som ska kopieras respekteras alltid.

`\copyfitmaxlines` trunkerar alltid extra utdatarader som överskrider den angivna gränsen. Det angivna antalet rader kommer aldrig att överskridas, även om det finns explicita radbrytningar. I den här versionen av Image Serving får det inte finnas fler än N-1 `\line`-markörer i det kopieringsanpassade textintervallet. Beteendet är odefinierat om den här gränsen överskrids.

## Exempel {#section-f4ddbbfade444560be30a813d90c2c1b}

I följande exempel antas att textens kropp har variablerna *[!DNL $A$]*, *[!DNL $B$]* och *[!DNL $C$]*.

**Behåll samma proportion mellan teckensnittsstorlekarna i hela intervallet:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* återges alltid dubbelt så stort som resten av texten. När mycket text anges återges *[!DNL $A$]* och *[!DNL $C$]* med `\fs10` och *[!DNL $B$]* med `\fs20`. Med liten text kommer *[!DNL $A$]* och *[!DNL $C$]* att använda `\fs100` och *[!DNL $B$]* `\fs200`.

**Konvertera till en vanlig stor teckenstorlek om bara en liten del av texten ritas:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

I den minsta änden av intervallet återges *[!DNL $B$]* med `\fs20`, dubbelt så stort som *[!DNL $A$]* och *[!DNL $C$]* vid `\fs10`. All text ritas vid `\fs100` (50 punkter) i den motsatta änden av intervallet.

**Konvertera till en vanlig liten teckenstorlek om mycket text ska återges:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

All text ritas med \fs10 i den lilla änden av intervallet, medan *[!DNL $A$]* och *[!DNL $C$]* återges med `\fs100` och *[!DNL $B$]* med `\fs200`.

**Inaktivera textpassning för ett inre textintervall:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

Teckensnittsstorleken för *[!DNL $A$]* och *[!DNL $C$]* kan variera mellan 10 och 100, medan *[!DNL $B$]* alltid återges med `\fs50`.

**Begränsa utdata till en enda rad, även om det finns mer lodrätt utrymme, men tillåt att det flödar över till ytterligare rader om för mycket text har angetts för att passa in på en enda rad vid  `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Begränsa utdata till en enda rad, även om det finns mer lodrätt utrymme. Om för mycket text har angetts för att få plats på en rad vid `\fs10` kommer den att trunkeras:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
