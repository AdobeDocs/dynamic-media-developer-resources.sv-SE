---
title: färg
description: Lagerfärg. Anger förgrundsfärgen och opaciteten för heltäckande färg- och effektlager samt textrutans fyllningsfärg för textlager.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# färg{#color}

Lagerfärg. Anger förgrundsfärgen och opaciteten för heltäckande färg- och effektlager samt textrutans fyllningsfärg för textlager.

` color= *`färg`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> färg </span> </span> </p> </td> 
  <td class="stentry"> <p>Grå, RGB eller CMYK-färgvärde, med eller utan alfa. </p> </td> 
 </tr> 
</table>

Om det finns bild- och textlager `color=` fyller genomskinliga och halvgenomskinliga områden inom lagrets begränsningsram med den angivna färgen* före* `rotate=` och `extend=` används.

## Egenskaper {#section-d6e74c36a49547849212e4db8927e678}

Lagerattribut. Gäller för aktuellt lager eller för lager 0 om `layer=comp`.

Modifieraren *`color`* antas finnas i den arbetsfärgrymd som motsvarar pixeltypen för *`color`*. Och *`color`* konverteras korrekt om lagerbilden har en annan pixeltyp vid tidpunkten för sammanslagningen.

## Standard {#section-60611c72876b4c45b5c85ce35608e5ec}

Ingen standard för enfärgade lager och effektlager. En färg måste anges. Standardvärdet är 0,0,0,0 (helt genomskinlig) för bild- och textlager.

## Exempel {#section-2d090493f4ec4e188bbc5565aa151a05}

I följande mallfragment är textbakgrunden inställd på en 50 % ogenomskinlig färg och använder samma färg för att lägga till en halvgenomskinlig kant på 10 pixlar runt bilden i lager 2:

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Se även {#section-f0e059f857b64b61ab4f23312b8dc619}

[färg](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Färghantering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
