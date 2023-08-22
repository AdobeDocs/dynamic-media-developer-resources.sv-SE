---
title: textFlowPath
description: Textflödesområde. Anger ett eller flera områden i vilka text som anges med textPs= ska flödas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b5575d17-150b-421c-b298-077b577eb95c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# textFlowPath{#textflowpath}

Textflödesområde. Anger ett eller flera områden i vilka text som anges med textPs= ska flödas.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition </span> </p> </td> 
  <td class="stentry"> <p>Bandata. </p> </td> 
 </tr> 
</table>

Se [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) ytterligare information, inklusive en beskrivning av *`pathDefinition`*.

RTF-marginalkommandon `\margl`, `\margr`, `\margt`och `\margb` ignoreras när `textFlowPath=` är närvarande. Om ingen sökvägsdefinition har angetts `textFlowPath=` ignoreras.

## Egenskaper {#section-b68dc887c6534ce8982cad740b3aeaa4}

Textlagerattribut ( `textPs=` endast). Ignoreras av andra lager. Gäller för `layer=0` om angivet för `layer=comp`.

## Standard {#section-68c4559b9e8242059b82e5a39a455dfc}

Samma som lagerrektangeln. Texten fyller hela lagrets rektangel.

## Se även {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15), [Textlager](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
