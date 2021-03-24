---
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
title: CallToAction.direction
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 1%

---


# CallToAction.direction{#calltoaction-direction}

Konfigurationsattribut för Interactive Video Viewer.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Anger hur miniatyrbilder fylls i vyn. </p> <p>Ange <span class="codeph"> vänster </span> för att ange fyllningsordningen vänster till höger. </p> <p>Om du anger <span class="codeph"> till höger </span> inverteras ordningen så att vyn fylls i från höger till vänster, uppifrån och ned. </p> <p>Ange <span class="codeph"> auto </span> om du vill att komponenten ska använda rätt läge när språkinställningen är <span class="codeph"> "ja" </span>; i annat fall används <span class="codeph"> vänster </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```

