---
description: Textflödesområde. Anger ett eller flera områden i vilka text som anges med textPs= ska flödas.
seo-description: Textflödesområde. Anger ett eller flera områden i vilka text som anges med textPs= ska flödas.
seo-title: textFlowPath
solution: Experience Manager
title: textFlowPath
topic: Scene7 Image Serving - Image Rendering API
uuid: 5449d78f-e56b-4afb-a05a-7cf8f1f37278
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# textFlowPath{#textflowpath}

Textflödesområde. Anger ett eller flera områden i vilka text som anges med textPs= ska flödas.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition  </span> </p> </td> 
  <td class="stentry"> <p>Bandata. </p> </td> 
 </tr> 
</table>

Se [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) om du vill ha mer information, inklusive en beskrivning av *`pathDefinition`*.

RTF-marginalkommandona `\margl`, `\margr`, `\margt` och `\margb` ignoreras när `textFlowPath=` finns. Om ingen sökvägsdefinition anges ignoreras `textFlowPath=`.

## Egenskaper {#section-b68dc887c6534ce8982cad740b3aeaa4}

Textlagerattribut ( `textPs=` endast). Ignoreras av andra lager. Gäller för `layer=0` om det anges för `layer=comp`.

## Standard {#section-68c4559b9e8242059b82e5a39a455dfc}

Samma som lagerrektangeln, text fyller hela lagrets rektangel.

## Se även {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15),  [textlager](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
