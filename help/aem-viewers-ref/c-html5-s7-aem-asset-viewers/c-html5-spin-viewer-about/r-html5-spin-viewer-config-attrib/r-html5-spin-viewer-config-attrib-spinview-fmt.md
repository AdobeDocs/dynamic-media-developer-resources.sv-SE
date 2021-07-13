---
description: SpinView.fmt
solution: Experience Manager
title: SpinView.fmt
feature: Dynamic Media Classic,Visningsprogram,SDK/API,snurra uppsättningar
role: Developer,User
exl-id: 3927d626-db16-4d30-80d3-5f63c3e9a110
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 1%

---

# SpinView.fmt{#spinview-fmt}

`[SpinView.|<containerId>_spinView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som komponenten använder för att läsa in bilder från Image Server. Om det angivna formatet slutar med <span class="codeph"> -alpha</span> återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. Komponenten har som standard en vit bakgrund. För att göra den genomskinlig anger du därför CSS-egenskapen <span class="codeph"> background-color</span> som <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-924163cb2f6542499f49894becef7fb5}

Valfritt.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`jpeg`

## Exempel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`fmt=png-alpha`
