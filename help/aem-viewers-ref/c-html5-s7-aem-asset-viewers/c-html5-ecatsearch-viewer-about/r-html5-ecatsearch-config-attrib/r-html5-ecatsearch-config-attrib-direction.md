---
title: riktning
description: riktning
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# riktning{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Anger hur sidor visas i huvudvyn och i miniatyrbilder. Det anger också hur användaren interagerar med visningsprogrammets användargränssnitt för att växla mellan katalogbildrutor. </p> <p>När <span class="codeph"> vänster </span> används anges högerjustering för den inledande sidan och vänsterjustering för den sista sidan. Det sammanfogar enskilda sidunderbilder för återgivningsordningen vänster till höger. Den ställer också in huvudvyn så att höger-till-vänster-bildruteanimering används för att flytta fram katalogen (om <span class="codeph"> PageView.frametransition </span> är inställd på bild). Slutligen ställs miniatyrerna in för en fyllningsordning från vänster till höger. </p> <p>När <span class="codeph"> right </span> används anges på liknande sätt en vänsterjustering för den inledande sidan och en högerjustering för den sista sidan. Det sammanfogar enskilda sidunderbilder för återgivningsordningen höger till vänster. Den ställer också in huvudvyn så att animering från vänster till höger används för att flytta fram katalogen (om <span class="codeph"> PageView.frametransition </span> är inställd på bild). Slutligen ändras ordningen på miniatyrbilderna så att miniatyrbildsvyn fylls i från höger till vänster, uppifrån och ned. </p> <p>När <span class="codeph"> auto </span> är inställt använder visningsprogrammet läget <span class="codeph"> right </span> när språkområdet är inställt på <span class="codeph"> ja. I annat fall använder det <span class="codeph"> left </span> -läge. </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-a66ce10d6c0b449883f654e7e0657e2c}

Valfritt.

## Standard {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Exempel {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
