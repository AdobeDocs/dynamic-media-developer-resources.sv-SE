---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
feature: Dynamic Media Classic,Visningsprogram,SDK/API,blandade medieuppsättningar
role: Developer,User
exl-id: c2aeb45f-879b-4a53-b571-744fc73d04fd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Anger om en ändring av rotationsriktningen ska tillåtas när en tvådimensionell rotation används. </p> <p>När den anges till <span class="codeph"> 1 </span> identifierar komponenten den primära dragnings- eller dragriktningen (vågrät eller lodrät) i början av gesten. Därefter behåller den riktningen tills gesten avslutas. Om användaren till exempel startar ett vågrätt snurra och sedan bestämmer sig för att fortsätta dra-gesten lodrätt, utförs ingen lodrät snurra i komponenten. I stället beaktas endast musens eller dragningens horisontella rörelse. </p> <p>Med värdet <span class="codeph"> 0 </span> kan användaren ändra rotationsriktning när som helst under gestförloppet. Inställningen påverkar inte om rotationsuppsättningen är 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
