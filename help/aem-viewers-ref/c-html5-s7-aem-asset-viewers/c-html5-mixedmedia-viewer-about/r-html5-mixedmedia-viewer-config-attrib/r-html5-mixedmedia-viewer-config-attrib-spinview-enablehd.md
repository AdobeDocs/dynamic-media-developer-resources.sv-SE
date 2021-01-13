---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
topic: Dynamic media
uuid: 3e7cdb44-4366-4e84-a6c7-c1cf1f5e6344
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '81'
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
