---
description: Färga bilden. Färglägger bilddata samtidigt som skuggor och högdagrar bevaras.
seo-description: Färga bilden. Färglägger bilddata samtidigt som skuggor och högdagrar bevaras.
seo-title: op_colorize
solution: Experience Manager
title: op_colorize
topic: Scene7 Image Serving - Image Rendering API
uuid: e74a85ca-73bf-4c69-ac77-768a58b33d0b
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---


# op_colorize{#op-colorize}

Färga bilden. Färglägger bilddata samtidigt som skuggor och högdagrar bevaras.

` op_colorize= *``*[,off|norm[, *`färgkontrast`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> färg  </span> </p> </td> 
  <td class="stentry"> <p>Ersätt RGB-färg. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> av  </span> </p> </td> 
  <td class="stentry"> <p>Inaktivera automatisk intensitetskompensation. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norm  </span> </p> </td> 
  <td class="stentry"> <p>Aktivera automatisk intensitetskompensation (standard). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> kontrast  </span> </p> </td> 
  <td class="stentry"> <p>Kontrastintervall (reellt 0.100). anges till 0 för att bevara indatakontrasten. </p> </td> 
 </tr> 
</table>

Det andra argumentet anger om källbildens intensitet ska justeras före färgläggning. Ange `off` om du vill inaktivera den automatiska intensitetskompensationen eller `norm` om du vill justera intensiteten automatiskt så att medianvärdet har intensiteten 50 %.

Ange värdet *`contrast`* till 0 om du vill bevara kontrastintervallet för indatabilden eller ange ett önskat kontrastintervall med ett värde som är större än 0. Värdet 100 maximerar kontrasten. Normala värden kan vara mellan 30 och 70.

Förutom de inbyggda justeringarna för ljusstyrka och kontrast kan `op_brightness=` och `op_contrast=` användas för att ytterligare finjustera färgeffekten.

>[!NOTE]
>
>Färgningsalgoritmen använder bara luminansinformationen i bilddata. Konverteringen till gråskala är enkel och inte färghanterad. `op_colorize` skickar alltid RGB-data, även om indata är gråskala eller CMYK.

## Egenskaper {#section-c0f8bd424b864153a1108f384939f55b}

Lager, kommando. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager.

*`color`* måste vara ett RGB-värde, grå- eller CMYK- *`color`* värden stöds inte.

Värdet *`contrast`* ignoreras om intensitetskompensationen är inaktiverad.

*`color`* antas finnas i den arbetsfärgrymd som motsvarar pixeltypen för  *`color`*. *`color`* konverteras korrekt om lagerbilden har en annan pixeltyp vid tidpunkten för sammanslagningen.

CMYK-bilder konverteras till RGB innan åtgärden tillämpas.

## Standard {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, utan färgsättning. Det andra och tredje argumentet är som standard `norm,0`, vilket ger automatisk intensitetskompensation och ingen kontraständring.

## Exempel {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Justera intensitet och kontrast dynamiskt innan du färglägger ett bildlager:

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

Använd automatisk justering av intensitet och kontrast i stället:

... `&op_colorize=a0b0c0,norm,50&`...

## Se även {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a),  [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d),  [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
