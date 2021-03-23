---
description: Parametern är gemensam för alla visningsprogram.
seo-description: Parametern är gemensam för alla visningsprogram.
seo-title: videoServerUrl
solution: Experience Manager
title: videoServerUrl
uuid: ef9870f9-599b-449d-b713-66abafb80311
feature: Dynamic Media Classic,visningsprogram,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---


# videoServerUrl{#videoserverurl}

Parametern är gemensam för alla visningsprogram.

>[!NOTE]
>
>Det här kommandot gäller inte för Video Image Viewer.

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Rotsökvägen till videoservern. Om ingen domän anges tillämpas i stället domänen som sidan hanteras från. Standard-URI-sökvägsupplösning gäller. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-10ee45d637134e0fbcd943c62578cb78}

Valfritt. Krävs inte för standardprogramvara som en serviceanvändning.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Exempel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```

