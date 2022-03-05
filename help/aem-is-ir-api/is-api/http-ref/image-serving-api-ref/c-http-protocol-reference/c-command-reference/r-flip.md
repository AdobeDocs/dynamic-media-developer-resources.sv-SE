---
description: Vänd lager. Vänder lagret vågrätt, lodrätt eller både och efter att beskärning= har använts och innan roate= och extend= har använts.
solution: Experience Manager
title: vända
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# vända{#flip}

Vänd lager. Vänder lagret vågrätt, lodrätt eller både och efter att beskärning= har använts och innan roate= och extend= har använts.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Vänd lagret vågrätt (vänster-höger). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Vänd lagret lodrätt (uppåt). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Vänd både vågrätt och lodrätt. </p> </td> 
 </tr> 
</table>

Kan även användas på textlager.

Vissa kommandon, inklusive `extend=`används automatiskt på lager 0 i stället för det sammansatta lagret när `layer=comp` är markerat. I sådana fall tillämpas alla kommandon som tilldelas automatiskt till lager 0 före de kommandon som gäller för `layer=comp`. När `layer=comp`, `extend=` används före `flip=`.

>[!NOTE]
>
>Det vända lagret placeras baserat på lagerankarpunkten. different flip=-värden ger olika lagerpositioner när ankarpunkten inte är placerad i mitten av lagret.

## Egenskaper {#section-294da2af7be746b5adfc35e29ee68217}

Lager, kommando. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager.

## Standard {#section-502044f81a89492198d5f12a738459ea}

Ingen.

## Se även {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
