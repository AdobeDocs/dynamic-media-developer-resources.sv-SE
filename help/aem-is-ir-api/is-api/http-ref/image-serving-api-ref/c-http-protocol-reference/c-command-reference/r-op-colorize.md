---
title: op_colorize
description: Färga bilden. Färglägger bilddata samtidigt som skuggor och högdagrar bevaras.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---

# op_colorize{#op-colorize}

Färga bilden. Färglägger bilddata samtidigt som skuggor och högdagrar bevaras.

` op_colorize= *`färg`*[,off|norm[, *`kontrast`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> färg </span> </p> </td> 
  <td class="stentry"> <p>Färg på RGB som ersättare. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> av </span> </p> </td> 
  <td class="stentry"> <p>Inaktivera automatisk ljusstyrkekompensation. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norm </span> </p> </td> 
  <td class="stentry"> <p>Aktivera automatisk ljusstyrkekompensation (standard). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> kontrast </span> </p> </td> 
  <td class="stentry"> <p>Kontrastintervall (reellt 0,100); angett till 0 för att bevara indatakontrasten. </p> </td> 
 </tr> 
</table>

Det andra argumentet anger om källbildens intensitet ska justeras före färgläggning. Ange `off` för att inaktivera automatisk ljusstyrkekompensation eller `norm` om du vill justera intensiteten automatiskt så att medianvärdet har intensiteten 50 %.

Ange *`contrast`* värdet 0 om du vill bevara kontrastintervallet för indatabilden eller ange ett önskat kontrastintervall med ett värde som är större än 0. Värdet 100 maximerar kontrasten. Standardvärdena kan vara mellan 30 och 70.

Förutom de inbyggda justeringarna för ljusstyrka och kontrast `op_brightness=` och `op_contrast=` kan användas för att ytterligare finjustera färgeffekten.

>[!NOTE]
>
>Färgningsalgoritmen använder bara luminansinformationen i bilddata. Konverteringen till gråskala är enkel och inte färghanterad. `op_colorize` matar alltid ut RGB-data, även om inmatningen är gråskala eller CMYK.

## Egenskaper {#section-c0f8bd424b864153a1108f384939f55b}

kommandot Lager. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager.

*`color`* måste vara ett RGB-värde; grått eller CMYK *`color`* värden stöds inte.

The *`contrast`* värdet ignoreras om intensitetskompensation är inaktiverad.

*`color`* antas finnas i den arbetsfärgrymd som motsvarar pixeltypen för *`color`*. *`color`* konverteras korrekt om lagerbilden har en annan pixeltyp vid tidpunkten för sammanslagningen.

CMYK-bilder konverteras till RGB innan åtgärden tillämpas.

## Standard {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, utan färgsättning. Det andra och tredje argumentet är som standard `norm,0`, för automatisk intensitetskompensation och utan kontraständring.

## Exempel {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Justera intensitet och kontrast dynamiskt innan du färglägger ett bildlager:

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

Använd automatisk justering av intensitet och kontrast i stället:

… `&op_colorize=a0b0c0,norm,50&`…

## Se även {#section-5581eb0e03014fa795e8f078c60e6c8d}

[färg](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Färghantering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
