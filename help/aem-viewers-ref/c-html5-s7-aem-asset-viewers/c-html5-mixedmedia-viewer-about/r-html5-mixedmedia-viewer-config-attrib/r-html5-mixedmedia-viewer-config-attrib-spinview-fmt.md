---
description: SpinView.fmt
solution: Experience Manager
title: SpinView.fmt
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Mixa medieuppsättningar
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---


# SpinView.fmt{#spinview-fmt}

`[SpinView.|<containerId>_spinView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_68C0C3D5C60640DC9A8EE04EA685AB99"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som komponenten använder för att läsa in bilder från Image Server. Om det angivna formatet slutar med <span class="codeph"> -alpha</span> återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. </p> <p>Komponenten har som standard en vit bakgrund. För att göra den genomskinlig anger du därför CSS-egenskapen <span class="codeph"> background-color</span> som <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
