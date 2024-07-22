---
title: bgc
description: Bakgrundsfärg Anger den subtraktiva färgen för färgningsbara texturer och dekorfärger.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# bgc {#bgc}

Bakgrundsfärg Anger den subtraktiva färgen för färgningsbara texturer och dekorfärger.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> färg </span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB eller grått färgvärde. </p></td> 
 </tr> 
</table>

Bildåtergivningens texturfärgningsalgoritm är okomplicerad - komponentvärdena för `bgc=` subtraheras från värdena för texturpixlar. `color=` läggs till och resultatet klipps till `0,0,0` och `255,255,255`.

För typisk användning av texturfärgning kan värdet för `bgc=` vara den viktigaste eller dominerande färgen i texturbilden. Dynamic Media Image Authoring innehåller halvautomatiska verktyg som extraherar rimliga `bgc=` färgvärden från texturbilder.

När ett texturmaterial används på ett vinjetteringsobjekt som inte kan struktureras används `bgc=` som förgrundsfärg om `color=` inte anges.

## Egenskaper {#section-b2db6f147d7f443ba9f671de04c2ef19}

Materialattribut. Ignoreras av heltäckande färg och kabinettmaterial.

## Standard {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` Om materialet baseras på en katalogpost, annars `bgc=808080` (neutralt grått).

## Exempel {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Färglägg en klädväv vars textur har den dominerande RGB-färgen 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Se även {#section-de9958dd63a742b4b5d780c59a57da33}

[katalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
