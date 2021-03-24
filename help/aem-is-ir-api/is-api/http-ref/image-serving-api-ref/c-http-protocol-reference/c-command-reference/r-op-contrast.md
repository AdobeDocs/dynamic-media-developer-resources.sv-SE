---
description: Justera kontrast. Justerar bildens kontrast genom att öka intensiteten för pixlar med mer än 50 % intensitet och minska intensiteten för pixlar med mindre än 50 % intensitet.
solution: Experience Manager
title: op_contrast
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
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
