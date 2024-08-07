---
title: glans
description: Glansighet på materialets yta. Anger materialytans relativa glansighet. Används för att välja belysningskartan och styra återgivningen av glanseffekter och 3D-reflektioner.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# glans{#gloss}

Glansighet på materialets yta. Anger materialytans relativa glansighet. Används för att välja belysningskartan och styra återgivningen av glanseffekter och 3D-reflektioner.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val </span> </span> </p></td> 
  <td class="stentry"> <p>Glans (0...100 procent) eller -1 som standardvärde för glans (referens). </p></td> 
 </tr> 
</table>

Högre glansvärden ger vanligen starkare, skarpare reflektioner och om glanseffekterna aktiveras i vinjetteringen förstärks speglande högdagrar på materialytan, främst genom att belysningskontrasten ökas. Varje materialtyp ( `type=`) definierar en minimal och maximal återgivningseffekt. För vissa materialtyper (till exempel väggpapper) har `gloss=` minimal inverkan på återgivningseffektens utseende, medan effekten är betydligt mer uttalad för andra materialtyper (till exempel sten eller keramik).

Om `illum=-1` och vinjetteringen definierar flera belysningskartor väljer `gloss=` det belysningskarta som används för den aktuella återgivningsåtgärden. Renderaren väljer det belysningskarta vars glanvärde är närmast den angivna glansen.

`gloss=-1` Väljer referensglansvärdet för den valda belysningskartan, enligt vinjetteringens visningsegenskaper. Med det här värdet kan du vara säker på att belysningskartan används exakt som den ska, utan ytterligare ändringar, även om glanseffekter är aktiverade. Om `illum=-1` används referensglansvärdet för den första belysningskartan i vinjetteringsvyn.

## Egenskaper {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Materialattribut. Ignoreras om vinjetteringen inte definierar flera belysningskartor. Eller, om `illum=` anges, om vinjetteringen inte innehåller 3D-reflektionsdata. Eller om det aktuella objektet inte stöder 3D-reflektioner eller om glanseffekterna är inaktiverade i vinjetteringen.

## Standard {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` Om materialet är baserat på en katalogpost, annars referensglansen för standardbelysningskartan eller belysningskartan som anges av `illum=`.

## Se även {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [grov=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
