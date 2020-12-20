---
description: 'null'
seo-description: 'null'
seo-title: riktning
solution: Experience Manager
title: riktning
topic: Dynamic media
uuid: 185824c5-d6f2-4e1b-99ac-726a295ec5f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---


# riktning{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>Anger hur sidor visas i huvudvyn och i miniatyrbilder. Det anger också hur användaren interagerar med visningsprogrammets användargränssnitt för att växla mellan katalogbildrutor. </p> <p>När <span class="codeph"> vänster </span> används anges högerjustering för den inledande sidan och vänsterjustering för den sista sidan. Det sammanfogar enskilda sidunderbilder för återgivningsordningen vänster till höger. Den ställer också in huvudvyn så att höger-till-vänster-bildruteanimering används för att flytta fram katalogen (om <span class="codeph"> PageView.frametransition </span> är inställd på bildruta). Slutligen ställs miniatyrerna in för en fyllningsordning från vänster till höger. </p> <p>När <span class="codeph"> höger </span> används anger den på samma sätt en vänsterjustering för den inledande sidan och högerjustering för den sista sidan. Det sammanfogar enskilda sidunderbilder för återgivningsordningen höger till vänster. Den ställer också in huvudvyn så att animering från vänster till höger används för att flytta fram katalogen (om <span class="codeph"> PageView.frametransition </span> är inställd på bildruta). Slutligen ändras ordningen på miniatyrbilderna så att miniatyrbildsvyn fylls i från höger till vänster, uppifrån och ned. </p> <p>När <span class="codeph"> auto </span> är inställt använder visningsprogrammet läget <span class="codeph"> right </span> när språkområdet är inställt på <span class="codeph"> ja; </span>I annat fall används det vänstra <span class="codeph">-läget.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-a66ce10d6c0b449883f654e7e0657e2c}

Valfritt.

## Standard {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Exempel {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
