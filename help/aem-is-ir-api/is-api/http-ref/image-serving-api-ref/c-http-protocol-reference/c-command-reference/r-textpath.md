---
title: textPath
description: Textbana. Anger sökvägen som ska användas som baslinje för texten som tillhandahålls med textPs=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# textPath{#textpath}

Textbana. Anger sökvägen som ska användas som baslinje för texten som tillhandahålls med textPs=.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition </span> </p> </td> 
  <td class="stentry"> <p>Bandata. </p></td> 
 </tr> 
</table>

Mer information, inklusive en beskrivning av *`pathDefinition`*, finns i [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d).

>[!NOTE]
>
>Förutom `clipPath=` stängs inte textbanor automatiskt när z eller Z inte anges i slutet av en underbana.

*`pathDefinition`* kan innehålla flera undersökvägar. Texten återges i de underordnade banorna i den angivna ordningen.

RTF-kommandona `\ql`, `\qc`, `\qr`, `\li` och `\ri` kan användas för att placera den återgivna texten längs banan.

## Egenskaper {#section-068137df436c46b9b55d271eb60e7285}

Textlagerattribut (endast `textPs=`). Ignoreras av andra lager. Gäller för `layer=0` om det anges för `layer=comp`. Ignoreras om `textPs=` finns.

Ett fel returneras om ett lager innehåller både `textPath=` och `textFlowPath=`.

## Standard {#section-697b1f2cfc43498080a31327e6eb173d}

Ingen, för standardtextåtergivning.

## Se även {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textlager](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
