---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
topic: Dynamic media
uuid: feeb02c0-f3f9-4559-acd9-cad30788b70b
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`varaktighet`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bild|sväng|auto</span> </p> </td> 
   <td colname="col2"> <p> Anger vilken typ av effekt som används vid bildruteändring. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> Med </span> bildrutor inaktiveras en övergång där den gamla bildrutan inte syns och den nya bildrutan visas. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> Med </span> vändning kan du aktivera en sidvändningseffekt när en användare kan dra i ett av de fyra uppslagshörnen och utföra en interaktiv sidvändning. </p> <p>När <span class="codeph"> tur</span> används kontrolleras komponentens utseende med modifieraren <span class="codeph"> pageturnstyle</span> och CSS-klassen <span class="codeph"> .s7pagedivider</span> ignoreras. </p> <p>Obs!  <p><span class="codeph"> Det finns inte stöd för </span> vändanimering i Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> automatiskt </span> ställer in övergången för vändbara bildrutor på stationära datorer och bildruteövergången på pekenheter. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> varaktighet</span></span> </p> </td> 
   <td colname="col2"> <p>Anger längden i sekunder för en <span class="codeph">-bildruta</span> eller <span class="codeph">-sväng</span>-övergångseffekt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-4d25a3f483834d2b9586fa70270ce6bd}

Valfritt.

## Standard {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Exempel {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
