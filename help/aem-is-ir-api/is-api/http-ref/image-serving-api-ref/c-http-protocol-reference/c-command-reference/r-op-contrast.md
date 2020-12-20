---
description: Justera kontrast. Justerar bildens kontrast genom att öka intensiteten för pixlar med mer än 50 % intensitet och minska intensiteten för pixlar med mindre än 50 % intensitet.
seo-description: Justera kontrast. Justerar bildens kontrast genom att öka intensiteten för pixlar med mer än 50 % intensitet och minska intensiteten för pixlar med mindre än 50 % intensitet.
seo-title: op_contrast
solution: Experience Manager
title: op_contrast
topic: Scene7 Image Serving - Image Rendering API
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# op_contrast{#op-contrast}

Justera kontrast. Justerar bildens kontrast genom att öka intensiteten för pixlar med mer än 50 % intensitet och minska intensiteten för pixlar med mindre än 50 % intensitet.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Kontrastjustering i procent (-100...100 int). </p></td> 
 </tr> 
</table>

## Egenskaper {#section-d319ed55057344eab0a3c93f720acdbf}

Lager, kommando. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager.

## Standard {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, utan att kontrasten förändras. CMYK-bilder eller -lager konverteras till RGB innan åtgärden tillämpas.

## Exempel {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Minska kontrasten och skärpan i ett bildlager med högre kvalitet för att visuellt matcha det mot ett bakgrundsfoto med låg kvalitet:

… `&op_blur=3&op_contrast=-12&`

I en framtida version kan bildens medianljusstyrka användas i stället för en fast intensitet på 50 %.
