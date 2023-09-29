---
title: vända
description: Vänd lager. Vänder lagret vågrätt, lodrätt eller både och efter att beskärning= har använts och innan roate= och extend= har använts.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
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
  <td class="stentry"> <p>Vänd både horisontellt och vertikalt. </p> </td> 
 </tr> 
</table>

Den kan också användas på textlager.

Vissa kommandon, inklusive `extend=`, används implicit på lager 0 i stället för det sammansatta lagret när `layer=comp` är markerat. I sådana fall tillämpas alla kommandon som tilldelas automatiskt till lager 0 före de kommandon som gäller för `layer=comp`. När `layer=comp`, `extend=` används före `flip=`.

>[!NOTE]
>
>Det vända lagret placeras baserat på lagerankarpunkten. Annat `flip=` värden resulterar i olika lagerpositioner när ankarpunkten inte är i mitten av lagret.

## Egenskaper {#section-294da2af7be746b5adfc35e29ee68217}

kommandot Lager. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager.

## Standard {#section-502044f81a89492198d5f12a738459ea}

Ingen.

## Se även {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
