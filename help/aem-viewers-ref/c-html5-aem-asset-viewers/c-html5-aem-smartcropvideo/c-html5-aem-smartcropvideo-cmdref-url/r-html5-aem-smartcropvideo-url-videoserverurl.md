---
description: URL-kommando för visningsprogrammet för smart beskärning.
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 945c32e0-a67b-4c27-b661-26510615d757
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 1%

---

# videoServerUrl{#videoserverurl}

URL-kommando för visningsprogrammet för smart beskärning.

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
videoServerUrl=http://s7d1.scene7.com/is/content/
```
