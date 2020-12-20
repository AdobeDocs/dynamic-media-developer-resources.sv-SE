---
description: Katalogdatafiler kan ha vilket namn och filsuffix som helst (förutom .ini).
seo-description: Katalogdatafiler kan ha vilket namn och filsuffix som helst (förutom .ini).
seo-title: Katalogdatafiler
solution: Experience Manager
title: Katalogdatafiler
topic: Scene7 Image Serving - Image Rendering API
uuid: 33d991d6-5aa7-4cc6-88d4-10c4bb83d786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---


# Katalogdatafiler{#catalog-data-files}

Katalogdatafiler kan ha vilket namn och filsuffix som helst (förutom .ini).

Katalogdatafiler kan enkelt underhållas med program som har stöd för tabbavgränsade textdatafiler som Microsoft Excel och Access.

En katalogdatafil är i princip en tvådimensionell tabell och består av en rubrikpost som identifierar datakolumner och ett valfritt antal dataposter (rader). Fält i både huvud- och dataposter avgränsas med enkla `<TAB>`-tecken. Posterna avgränsas med en enda `<CR>` (ASCII-kod 0xD), en enda `<LF>` (ASCII-kod 0xA) eller ett `<CR><LF>`-par.

Rubrikposten måste innehålla de exakta namnen för varje datafält. Tomma fält tillåts inte i rubrikraden. Datafältnamn är inte skiftlägeskänsliga. Alla fältnamn måste vara unika.

Inget annat tomt utrymme än fältavgränsarna `<TAB>` tillåts i rubrik- och dataposter.

I dataposterna anger två intilliggande `<TAB>`-tecken ett tomt fält. Tomma fält ärver standardvärden från antingen katalogattributen eller serverstandardvärdena.

Datafälten får inte innehålla `<CR>`, `<LF>` eller `<TAB>` tecken, såvida inte datavärdet är av typen text och omsluts av enkla eller dubbla citattecken. Datafälten får inte vara HTTP-kodade.

Flera datavärden i samma fält avgränsas med kommatecken (&#39;,&#39;), om inget annat anges.

Kolumner vars namn börjar med &#39;.&#39; ignoreras, Detta gör det möjligt att lagra data i materialkataloger som inte är av intresse för bildåtergivning. Kolumner med okända rubriknamn ignoreras och en varning skrivs till loggfilen.

Fältnamn kan bestå av en valfri kombination av ASCII-bokstäver, siffror samt &quot;-&quot; och &quot;_&quot;.

En eller flera kolumner kan användas som indexnycklar. Om samma tangent förekommer mer än en gång i samma datafil gäller den senare instansen.
