---
description: Exkluderingsområde för textflöde. Anger ett eller flera områden som ska uteslutas från textflödet.
seo-description: Exkluderingsområde för textflöde. Anger ett eller flera områden som ska uteslutas från textflödet.
seo-title: textFlowXPath
solution: Experience Manager
title: textFlowXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: ce833ae7-e774-4954-a521-b6247e75f6eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---


# textFlowXPath{#textflowxpath}

Exkluderingsområde för textflöde. Anger ett eller flera områden som ska uteslutas från textflödet.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Bandata. </p></td> 
 </tr> 
</table>

Se [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) om du vill ha mer information, inklusive en beskrivning av *`pathDefinition`*. Om ingen sökvägsdefinition anges ignoreras `textFlowXPath=`.

## Egenskaper {#section-cd1ebb151d4a405fbfc508d46522d686}

Textlagerattribut ( `textPs=` endast). Ignoreras av andra lager eller när det anges utan `textFlowPath=`. Gäller för `layer=0` om det anges för `layer=comp`.

## Standard {#section-9405cda904684d829ed12a9e40a4dc46}

Ingen.

## Se även {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
