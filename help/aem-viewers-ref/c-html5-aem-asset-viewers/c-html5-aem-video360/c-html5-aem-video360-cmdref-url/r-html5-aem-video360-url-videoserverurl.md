---
description: URL-kommando för Video360 Viewer.
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,visningsprogram,SDK/API,360 VR-video
role: Utvecklare,Affärsledare
exl-id: 76204d0a-449b-4fe5-a2aa-36739fab482f
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# videoServerUrl{#videoserverurl}

URL-kommando för Video360 Viewer.

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Rotsökvägen till videoservern. Om ingen domän anges tillämpas i stället domänen som sidan hanteras från. Standard-URI-sökvägsupplösning gäller. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt. Krävs inte för standardanvändning av SaaS.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d9.scene7.com/is/content/
```
