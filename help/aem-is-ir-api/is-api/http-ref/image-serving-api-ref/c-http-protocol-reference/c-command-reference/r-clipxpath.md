---
description: Inverterad lagerklippbana. Anger en exkluderingsklippbana för det aktuella lagret. Alla delar av lagret som ligger inom det område som definieras av clipXPath= återges som genomskinliga.
seo-description: Inverterad lagerklippbana. Anger en exkluderingsklippbana för det aktuella lagret. Alla delar av lagret som ligger inom det område som definieras av clipXPath= återges som genomskinliga.
seo-title: clipXPath
solution: Experience Manager
title: clipXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a4062f3f-5dba-4514-acde-e1b7d608a2e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# clipXPath{#clipxpath}

Inverterad lagerklippbana. Anger en exkluderingsklippbana för det aktuella lagret. Alla delar av lagret som ligger inom det område som definieras av clipXPath= återges som genomskinliga.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span></span> </p> </td> 
  <td class="stentry"> <p>Bandata. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Namnet på banan som är inbäddad i lagerkällbilden (endast ASCII). </p></td> 
 </tr> 
</table>

Mer information finns i [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) , inklusive en beskrivning av ` *`pathName`*` och ` *`pathDefinition`*`.

## Egenskaper {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Lagerattribut. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras om `clipPath=` inte anges. Ignoreras av effektlager.

## Standard {#section-d1986aa31af14767aeb1b4a57add67f4}

Ingen.

## Se även {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
