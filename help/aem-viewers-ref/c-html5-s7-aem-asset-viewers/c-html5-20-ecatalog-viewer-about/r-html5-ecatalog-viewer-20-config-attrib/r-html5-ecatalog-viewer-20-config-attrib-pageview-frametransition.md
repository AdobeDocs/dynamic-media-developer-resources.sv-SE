---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
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
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> bild</span> aktiverar en övergång där den gamla bildrutan inte syns och den nya bildrutan visas. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> sväng</span> aktiverar en sidvändningseffekt när en användare kan dra i ett av de fyra uppslagshörnen och utföra en interaktiv sidvändning. </p> <p>När <span class="codeph"> sväng</span> används om komponentens utseende styrs av <span class="codeph"> pageturnstyle</span> modifierare och <span class="codeph"> .s7pagedivider</span> CSS-klassen ignoreras. </p> <p>Obs!  <p><span class="codeph"> sväng</span> Animering stöds inte på Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> anger övergången för vändbildruta på stationära datorer och bildövergången på pekenheter. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> varaktighet</span></span> </p> </td> 
   <td colname="col2"> <p>Anger längden i sekunder för en <span class="codeph"> bild</span> eller <span class="codeph"> sväng</span> övergångseffekt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-4d25a3f483834d2b9586fa70270ce6bd}

Valfritt.

## Standard {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Exempel {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
