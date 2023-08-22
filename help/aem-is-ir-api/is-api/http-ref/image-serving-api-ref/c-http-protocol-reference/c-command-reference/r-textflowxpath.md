---
title: textFlowXPath
description: Exkluderingsområde för textflöde. Anger ett eller flera områden som ska uteslutas från textflödet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '76'
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

Se [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) ytterligare information, inklusive en beskrivning av *`pathDefinition`*. Om ingen sökvägsdefinition har angetts `textFlowXPath=` ignoreras.

## Egenskaper {#section-cd1ebb151d4a405fbfc508d46522d686}

Textlagerattribut ( `textPs=` endast). Ignoreras av andra lager eller när den anges utan `textFlowPath=`. Gäller för `layer=0` om angivet för `layer=comp`.

## Standard {#section-9405cda904684d829ed12a9e40a4dc46}

Ingen.

## Se även {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
