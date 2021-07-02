---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
feature: Dynamic Media Classic,Visningsprogram,SDK/API,blandade medieuppsättningar
role: Developer,Business Practitioner
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 1%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`tal`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Aktivera, begränsa eller inaktivera optimering för enheter där <span class="codeph"> devicePixelRatio</span> är större än <span class="codeph"> 1</span>, det vill säga enheter med hög densitet som iPhone4 och liknande enheter. Om den är aktiv begränsar komponenten storleken på IS-bildbegäran som om enheten bara hade ett pixelförhållande på <span class="codeph"> 1</span> och minskar därför bandbredden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tal</span></span> </p> </td> 
   <td colname="col2"> <p> Om du använder inställningen <span class="codeph"> limit</span> aktiverar komponenten endast hög pixeldensitet upp till den angivna gränsen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
