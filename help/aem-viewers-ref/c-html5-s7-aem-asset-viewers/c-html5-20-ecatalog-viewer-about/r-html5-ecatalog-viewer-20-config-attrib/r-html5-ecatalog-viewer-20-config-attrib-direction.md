---
title: riktning
description: Anger hur sidor visas i huvudvyn och i miniatyrbilder. Det anger också hur användaren interagerar med visningsprogrammets användargränssnitt för att växla mellan katalogbildrutor.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7d3df37-3e8b-438f-8b24-035b6982dc14
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# riktning{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Anger hur sidor visas i huvudvyn och i miniatyrbilder. Det anger också hur användaren interagerar med visningsprogrammets användargränssnitt för att växla mellan katalogbildrutor. </p> <p>När <span class="codeph"> vänster </span> används för att ange högerjustering för den inledande sidan och vänsterjustering för den sista sidan. Det sammanfogar enskilda sidunderbilder för återgivningsordningen vänster till höger. Den ställer också in huvudvyn så att höger-till-vänster-animering används för att flytta fram katalogen (om det är <span class="codeph"> PageView.frametransition </span> är inställt på bildruta). Slutligen ställs miniatyrerna in för en fyllningsordning från vänster till höger. </p> <p>På samma sätt när <span class="codeph"> höger </span> används för att ange vänsterjustering för den inledande sidan och högerjustering för den sista sidan. Det sammanfogar enskilda sidunderbilder för återgivningsordningen höger till vänster. Den ställer också in huvudvyn så att animering från vänster till höger används för att flytta fram katalogen (om det är <span class="codeph"> PageView.frametransition </span> är inställt på bildruta). Slutligen ändras ordningen på miniatyrbilderna så att miniatyrbildsvyn fylls i från höger till vänster, uppifrån och ned. </p> <p>När <span class="codeph"> auto </span> är inställt, används visningsprogrammet <span class="codeph"> höger </span> läge när språkinställningen är inställd på <span class="codeph"> ja, </span>annars används <span class="codeph"> vänster </span> läge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-a66ce10d6c0b449883f654e7e0657e2c}

Valfritt.

## Standard {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Exempel {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
