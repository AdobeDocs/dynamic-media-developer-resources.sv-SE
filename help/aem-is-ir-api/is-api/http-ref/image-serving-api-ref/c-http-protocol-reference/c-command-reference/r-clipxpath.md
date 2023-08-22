---
title: clipXPath
description: Inverterad lagerklippbana. Anger en exkluderingsklippbana för det aktuella lagret. Alla delar av lagret som ligger inom det område som definieras av clipXPath= återges som genomskinliga.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# clipXPath{#clipxpath}

Inverterad lagerklippbana. Anger en exkluderingsklippbana för det aktuella lagret. Alla delar av lagret som ligger inom det område som definieras av clipXPath= återges som genomskinliga.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Bandata. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>Namnet på banan som är inbäddad i lagerkällbilden (endast ASCII). </p></td> 
 </tr> 
</table>

Se [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) ytterligare information, inklusive en beskrivning av `*`pathName`*` och `*`pathDefinition`*`.

## Egenskaper {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Lagerattribut. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras om `clipPath=` har inte angetts. Ignoreras av effektlager.

## Standard {#section-d1986aa31af14767aeb1b4a57add67f4}

Ingen.

## Se även {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
