---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c2aeb45f-879b-4a53-b571-744fc73d04fd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Anger om en ändring av rotationsriktning ska tillåtas om det finns en tvådimensionell rotationsuppsättning. </p> <p>När inställt på <span class="codeph"> 1 </span>identifierar komponenten den primära dra- eller dragriktningen (vågrät eller lodrät) i början av gesten. Därefter behåller den riktningen tills gesten avslutas. Om användaren till exempel startar ett vågrätt snurra och sedan bestämmer sig för att fortsätta dra-gesten lodrätt, utförs ingen lodrät snurra i komponenten. I stället beaktas endast musens eller dragningens horisontella rörelse. </p> <p>Värdet för <span class="codeph"> 0 </span> gör att användaren kan ändra rotationsriktning när som helst under gestförloppet. Inställningen har ingen effekt om rotationsuppsättningen är 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
